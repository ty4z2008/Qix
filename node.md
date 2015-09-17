模块Github地址：https://github.com/felixge/node-mysql

微博:[@廖君Jun](http://weibo.com/ty4z2008)

自己还是一个学生，第一次翻译。不恰当的地方还希望不吝批评。联系方式可以直接微博AT我

##安装

```bash
npm install mysql
```

如果需要以前的版本0.9.x系列的文档，请访问[v0.9 branch]: https://github.com/felixge/node-mysql/tree/v0.9.

有时你可以从github中安装最新版本的node-mysql，具体怎么做请参考下面的示例：

```bash
npm install felixge/node-mysql
```

##介绍
这是一个node.Js的mysql驱动程序。这个驱动完全是用javascript写的，不需要任何编译工作。完全的遵守MIT开源协议。

这里有一个简单的示例告诉你如何使用它:

```js
var mysql      = require('mysql');
var connection = mysql.createConnection({
  host     : 'localhost',
  user     : 'me',
  password : 'secret',
  database : 'my_db'
});
connection.connect();//建立连接
connection.query('SELECT 1 + 1 AS solution', function(err, rows, fields) {
  if (err) throw err;
  console.log('The solution is: ', rows[0].solution);
});
connection.end();//释放连接
```

从上面这个例子中，你应该要知道如下的两点：

每个方法调用在连接队列中是按顺序执行。

当使用`end()`函数关闭连接时候，你必须要确保你的所有查询都已经发送给了mysql服务器。否者`end()`之后的查询是无效的。

##贡献者

非常感谢那些给这个模块开发作贡献的朋友[GitHub Contributors page][].


[GitHub Contributors page]: https://github.com/felixge/node-mysql/graphs/contributors

其中，我特别需要感谢的两位：

[Andrey Hristov][]  (Oracle) 与[Ulf Wendel][]帮我解决了一些数据库协议上面的问题

[Ulf Wendel]: http://blog.ulf-wendel.de/

[Andrey Hristov]: http://andrey.hristov.com/

##赞助商

特别的感谢下面这些公司在资金上面的赞助，让我能够有更多的时间在这个项目上面(下面的名次根据赞助时间排序)

* [Transloadit](http://transloadit.com) (我的首位赞助公司，他们公司主要是提供文件上传与视频转码服务，瞧瞧吧)
* [Joyent](http://www.joyent.com/)
* [pinkbike.com](http://pinkbike.com/)
* [Holiday Extras](http://www.holidayextras.co.uk/)  (他们正在招聘[hiring](http://join.holidayextras.co.uk/vacancy/software-engineer/))
* [Newscope](http://newscope.com/)  (他们正在招聘[hiring](http://www.newscope.com/stellenangebote))


如果你也对这个项目感兴趣，那么你也可以赞助我们，请点击[get in touch][].

[get in touch]: http://felixge.de/#consulting

##社区支持

如果你也想参与到这个模版讨论，或者是有问题需要询问，可以通过下面的方式来联系：

* **Google论坛**：https://groups.google.com/forum/#!forum/node-mysql
* **IRC频道**： #node.js (freenode.net,只要包含有mysql的所有问题我都会关注的)

##创建连接

推荐的一种连接方式：
```js
var mysql      = require('mysql');
var connection = mysql.createConnection({
  host     : 'example.org',
  user     : 'bob',
  password : 'secret'
});

connection.connect(function(err) {
  if (err) {
    console.error('error connecting: ' + err.stack);
    return;
  }

  console.log('connected as id ' + connection.threadId);
});
```
然而，一个连接只能隐式的调用一个`query`函数。调用方式如下：
```js
var mysql      = require('mysql');
var connection = mysql.createConnection(...);

connection.query('SELECT 1', function(err, rows) {
  //成功连接! (unless `err` is set)
});
```
 
上面的两种错误处理方法都合适，这取决于你更喜欢那一种方式来做数据库错误信息处理。任何一种连接上的错误（握手与网络）都会被视为致命错误，具体更多的错误处理信息可以查看[Error Handling](#error-handling)章节。

##连接可选参数
当我们使用Node-MySQL建立一个数据库连接的时候你可以通过下面这些选项：
* `host`:数据库的主机名（默认： `localhost`）
* `port`:数据库服务器的端口（默认： `3306`）
* `localAddress`:使用TCP连接的源IP地址（可选）
* `socketPath`:使用Unix域套接字连接的路径，当使用 `host` 与`port` 的时候可以忽略。
* `user`:这个是MySQL身份验证的用户名。
* `password`:MySQL用户的密码。
* `database`:连接的数据库名(可选).
* `charset`:连接之后的字符编码(默认:`UTF8_GENERAL_CI`,值得提醒的是，这个值必须都是大写字母).
* `timezone`:这个是储存数据的是当前时间。(默认:` local`).
* `connectTimeout`:MySQL初始连接的超时时间。单位是毫秒(默认:无超时限制)。
* `stringifyObjects`:把值转换为Stringify对象。具体见问题 [#501](https://github.com/felixge/node-mysql/issues/501)。(默认：`false`)。
* `insecureAuth`:允许使用老（不安全）的身份认证方式去连接MySQL数据库.(默认：` false`).
* `typeCast`:是否把结果值转换为原生的javascript类型(默认: `true`).
* `queryFormat`:一个可以自己定义查询格式函数(具体见[Custom format](#custom-format))。
* `supportBigNumbers`: 当在数据库中处理一个大数(`BIGINT`和`DECIMAL`)数据类型的时候，你需要启用这个选项(默认: `false`).
* `bigNumberStrings`:这个选项需要`bigNumberStrings`与 `supportBigNumbers`同时启用，强制把数据库中大数(BIGINT和DECIMAL)数据类型的值转换为javascript字符对象串对象返回。(默认:`false`)。当启用`supportBigNumbers`选项，但 `bigNumberStrings`是未启用的状态。当无法用javascript数字对象([JavaScript Number objects](http://ecma262-5.com/ELS5_HTML.htm#Section_8.5))所表达的时候就会返回的是一个big number字符串对象(值的范围要在 [-2^53, +2^53]之间).否则将会返回一个Number类型的对象。如果`supportBigNumbers`是`false`那么这个选项会被自动忽略。
* `dateStrings`:强制为date类型(`TIMESTAMP`，`DATETIME`，`DATE`)转化为一个字符串返回而不是转换成javascript的date类型对象。(默认: `false`)
* `debug`:答应协议详细信息到标准输出(默认: `false`).
* `trace`:产生栈跟踪当在库的入口点出现`error`时,当调用数次很多时性能会略微下降(默认: `true`).
* `multipleStatements`:允许每个mysql语句有多条查询.使用它时要非常注意，因为它很容易引起sql注入攻击(默认:`false`).
* `flags`:使用连接标示符号标示出超过默认的值的连接。它也可以加到默认的黑名单连接中。更多信息参考（[Connection Flags](#connection-flags)）。 
* `ssl`:使用`ssl`参数对象()或者是用一个包含ssl配置的字符串名。[SSL options](#ssl-options)

```
除了把这些选项写成对象的样式以外，你也可以用一个字符串来表示。例如：

```js
var connection = mysql.createConnection('mysql://user:pass@host/db?debug=true&charset=BIG5_CHINESE_CI&timezone=-0700');
```

注意：查询出来的值第一会尝试转换为json格式,如果转换失败.那么就会转换成纯文本的字符串.
###SSL
``ssl``参数在连接的选项里面可以是字符串或对象，当是一个字符串的时候它会使用已经存在的ssl证书。例如：
* `"Amazon RDS"`:目前仅仅支持亚马逊的ca证书，参考：https://rds.amazonaws.com/doc/rds-ssl-ca-cert.pem 
当连接到其他服务器的时候，你需要提供一个参数对象。格式可以参考[crypto.createCredentials](http://nodejs.org/api/crypto.html#crypto_crypto_createcredentials_details).请注意参数请求的证书是整个证书名(包括文件后缀),而不只是单单的文件名这里有一个简单的例子:
```js
var connection = mysql.createConnection({
  host : 'localhost',
  ssl  : {
    ca : fs.readFileSync(__dirname + '/mysql-ca.crt')
  }
});
```
你也可以不使用证书来建立数据库连接,但是你得把`rejectUnauthorized`设置为false
```js
var connection = mysql.createConnection({
  host : 'localhost',
  ssl  : {
    // DO NOT DO THIS
    // 设置正确的连接方式
    rejectUnauthorized: false
  }
});
```
##关闭连接
有两种关闭连接的方式，当查询完成后最优雅关闭连接方式是调用end()方法,例如：
 
```js
connection.end(function(err) {
  // 连接在这里会被终止
});
```
这样可以确保在查询队列完成之后发送一个`COM_QUIT` 包到mysql服务器。如果在发送`COM_QUIT`出现致命的错误。在回调函数里面有一个`err`参数可以使用。但是这个连接无论如何也会被关闭掉。

另外一种替代`end()`方法的是调用`destroy()`方法，这个方法会立即终止底层socket连接.`destroy()`方法确保了没有任何事件或回调再连接触发。
 
```js
connection.destroy();
```

`destroy()`方法不像`end()`方法， `destroy()`方法是没有任何回调参数的。

##连接池
直接使用连接池
 
```js
var mysql = require('mysql');
var pool  = mysql.createPool({
  host     : 'example.org',
  user     : 'bob',
  password : 'secret'
});

pool.query('SELECT 1 + 1 AS solution', function(err, rows, fields) {
  if (err) throw err;

  console.log('The solution is: ', rows[0].solution);
});

```

连接可以轻易的共享一个连接或者是管理多个连接：

```js
var mysql = require('mysql');
var pool  = mysql.createPool({
  host     : 'example.org',
  user     : 'bob',
  password : 'secret'
});
pool.getConnection(function(err, connection) {
  //连接成功!(除非有`err`)
});
```


如果你想在连接前设置session变量并且获取使用。你可以监听`connection`事件：
 
```js
pool.on('connection', function(connection) {
  connection.query('SET SESSION auto_increment_increment=1')
});
```
当你的连接完成后，只需要调用`connection.release()`方法。将连接返回到池中，以供其他人再次使用。
```js
var mysql = require('mysql');
var pool  = mysql.createPool(...);

pool.getConnection(function(err, connection) {
  //使用连接
  connection.query( 'SELECT something FROM sometable', function(err, rows) {
     //连接使用完成后释放连接
    connection.release();

    //不要在这里使用connection进行查询，因为连接已经被归还到连接池了
  });
});
```


如果你想关闭连接并且从连接池中移除，使用`connection.destory()`方法代替。当你下一次需要使用的时候，池会自动创建一个新的连接。
通过池创建连接是非常缓慢的。如果你配置你的连接池最大的连接数为100，当你只需要同时使用5个连接时候，它也仅仅只会创建5个连接。这种连接的循环方式是一种轮询(round-robin)的方式。采取的是从连接池顶部到底部的方式。

##Pool参数选项
池连可以接受一些连接的参数选项。当一个连接创建之后，这些参数选项通过简单的构造传递到连接里面。池连接参数可以接受下面这些参数。
* `waitForConnections`:判断当前的连接是否可用并且是否已经达到了连接数的上限。如果是`true`。这个连接就会加入到连接队列中同时把状态转换为可用状态。如果是`false`，那么会立即返回一个错误给开发者。(默认：`true`).
* `connectionLimit`:一次连接最大的连接数(默认:`10`)。
* `queueLimit`:从`getConnection`获取连接数并且判断是否超出了`queneLimit`限制的排队等待的连接值，如果是就返回一个错误。如果设置为`0`，就是不限制连队列数(默认：`0`)。

##PoolCluster
PoolCluster提供了多台主机连接功能(group&retry&selector)：

```js
//创建连接
var poolCluster = mysql.createPoolCluster();

poolCluster.add(config); // anonymous group
poolCluster.add('MASTER', masterConfig);
poolCluster.add('SLAVE1', slave1Config);
poolCluster.add('SLAVE2', slave2Config);

// 目标主机组 : ALL(anonymous, MASTER, SLAVE1-2), 连接方式 : round-robin(default)
poolCluster.getConnection(function (err, connection) {});

// 目标主机组 : MASTER, 连接方式: round-robin
poolCluster.getConnection('MASTER', function (err, connection) {});

// 目标主机组 : SLAVE1-2, 连接方式 : order
// 如果不能连接到SLAVE1就连接SLAVE2（把SLAVE1从集群节点中删除）
poolCluster.on('remove', function (nodeId) {
  console.log('REMOVED NODE : ' + nodeId); // nodeId = SLAVE1 
});

poolCluster.getConnection('SLAVE*', 'ORDER', function (err, connection) {});

// 命名方式: of(pattern, selector)
poolCluster.of('*').getConnection(function (err, connection) {});

var pool = poolCluster.of('SLAVE*', 'RANDOM');
pool.getConnection(function (err, connection) {});
pool.getConnection(function (err, connection) {});

// 释放连接
poolCluster.end();
```
 

##PoolCluster选项
* `canRetry`:如果是`true`,当连接失败时`Poolcluster`会尝试重新连接(默认:`true`)。
* `removeNodeErrorCount`:如果连接失败,节点的`errorCount`将会增加.当`errorCount`大于`removeNodeErrorCount`时，会从`poolCluster`中移除一个节点。(默认:`5`).
* `defaultSelector`:默认选择器(默认:`RR`).
* `RR`:选择一个交替(轮循)
* `RANDOM`：由随机函数选择一个节点.
* `ORDER`:按照顺序无条件的选择第一个节点。

```js
var clusterConfig = {
  removeNodeErrorCount: 1, // 连接失败后立即从把该节点移除
  defaultSelector: 'ORDER'
};

var poolCluster = mysql.createPoolCluster(clusterConfig);
```

##切换用户/修改连接状态
MySQL提供了ChangeUser的命令，允许你更改当前用户并且切换用户时不需要关闭底层socket连接:
```js
connection.changeUser({user : 'john'}, function(err) {
  if (err) throw err;
});
```
这个功能提供了几个有用的参数选项： 
* `user`:新用户的名字。（默认为切换新用户前第一个用户）
* `password`:新用户的密码（默认为切换新用户前第一个用户）
* `charset`:新的字符编码（默认为切换新用户前第一个用户）
* `database`:新的数据库名（默认为切换新用户前第一个用户）

这个功能有时有一个副作用，它会把所有的连接状态都重置（变量，事务）.
注意：此操作出现的错误会被该模块视为致命错误处理。

##服务器连接断开
由于网络问题你有可能丢失与MySQL服务器的连接。也有可能被服务器踢出连接，还有可能是服务器重启或是崩溃等等，这些都是致命的错误都被归为`error`对象里面。并且模块提供了`err.code = 'PROTOCOL_CONNECTION_LOST'`信息，更多的错误处理信息请参考[Error Handling](#error-handling) 。
与服务器重连是建立一个新的连接，一旦现在的连接断开就不能让这个连接重新连接。它必须重新建立一条连接，连接到数据库服务器。
在连接池里面，当连接断开时会从连接池里面把连接移除，当下次需要连接的时候调用`getConnection`创建一个新的连接。

转义查询值
为了避免被SQL注入攻击,你需要把用户提交过来的数据进行转义之后再放到SQL查询语句里面。模块提供了`connection.escape()`和`Pool.escape()`两种方法：
 
```js
var userId = 'some user provided value';
var sql    = 'SELECT * FROM users WHERE id = ' + connection.escape(userId);
connection.query(sql, function(err, results) {
  // ...
});
```
或者，你可以使用占位符`?`来代替，同样的也能对传入的值进行转义:
 
```js
connection.query('SELECT * FROM users WHERE id = ?', [userId], function(err, results) {
  // ...
});
```
这看起来像是使用了MySQL的预处理语句，其实同样的在MySQL内部也是使用了类似`connection.escape()`的方法。
**注意**这不同于MySQL预处理语句，因为它会把所有的`?`都替换掉.
不同的是类型转义的值不同。请看下面的解释:
* Number类型保存不变.
* Boolean值被转换为了`true/false`字符串.
* Date类型被转换为了`YYYY-mm-dd HH:ii:ss`字符串
* Buffer转换为了16进制，例如:`X'0fa5'`
* String转换为了安全的字符串。
* Array转换为了`list`。例如:`['a','b']`会返回`'a','b'`
多维数组会被转换为多维`list`。例如`[['a', 'b'], ['c', 'd']]`返回`('a', 'b'), ('c', 'd')`
* Object转换为`key = 'val'`;多维Object对象会转换为字符串.
* undefined/null会转换为`null`
* NaN / Infinity 保持不变,因为MySQL现在并不支持这些对象，如果你把`NaN/Infinity`做为值,MySQL会报错.直到它们被MySQL支持。

如果你留意了，你会发现转义查询值可以巧妙的用下面这种方式:

```js
var post  = {id: 1, title: 'Hello MySQL'};
var query = connection.query('INSERT INTO posts SET ?', post, function(err, result) {
  // Neat!
});
console.log(query.sql); // INSERT INTO posts SET `id` = 1, `title` = 'Hello MySQL'

```

如果你觉得有必要自己去转义查询值，那么你可以直接去调用转义函数：
 
```js
var query = "SELECT * FROM posts WHERE title=" + mysql.escape("Hello MySQL");

console.log(query); //SELECT * FROM posts WHERE title='Hello MySQL'
```

##转义查询标示符
如果你不信任用户提交过来的标示符(database/table/column name)。那么你需要使用mysql.escapeId(identifier)来转义:
```js
var sorter = 'date';
var query = 'SELECT * FROM posts ORDER BY ' + mysql.escapeId(sorter);

console.log(query); // SELECT * FROM posts ORDER BY `date`
```
它还支持添加合格的转义符。不过得把转义的分成两部分:
 
```js
var sorter = 'date';
var query = 'SELECT * FROM posts ORDER BY ' + mysql.escapeId('posts.' + sorter);

console.log(query); // SELECT * FROM posts ORDER BY `posts`.`date`
```

或者,你可以使用占位符`??`，它会自动转义查询的值：
 
```js
var userId = 1;
var columns = ['username', 'email'];
var query = connection.query('SELECT ?? FROM ?? WHERE id = ?', [columns, 'users', userId], function(err, results) {
  // ...
});

console.log(query.sql); // SELECT `username`, `email` FROM `users` WHERE id = 1
```

**请注意：最后的一个字符转义目前还在实验阶段，而且语法随时可能发生改变。**
当你使用`.escape()`,`.query()`,`.escapeId()`时可以有效的防御SQL注入攻击.
###预查询
你可以使用`mysql.format()`去执行预处理多嵌套查询语句，利用适当的转义处理对于标示符与值.下面有一个简单的例子:
 
```js
var sql = "SELECT * FROM ?? WHERE ?? = ?";
var inserts = ['users', 'id', userId];
sql = mysql.format(sql, inserts);
```
这种方法可以确保发送到数据库进行数据查询之前就能够保证查询语句的安全,在发送到数据库查询之前执行预查询，这个功能非常的有用。由于`mysql.format`是由sql的`String.format`暴露出来的。所以你可以你还可以选择传递`stringifyObject` 和`timezone`对象(不强制要求)。并且允许您自定义把对象转换字符串的方法。以及特定地区的时间和时区(`location  specific/timezone aware Date`).
###自定义格式
如果您喜欢其他样式的转义格式。你可以在连接配置选项中自定义你的功能函数。如果你还想使用`escape()`或其他内置的函数。可以直接调用
这儿我们提供了一个示例：
```js
connection.config.queryFormat = function (query, values) {
  if (!values) return query;
  return query.replace(/\:(\w+)/g, function (txt, key) {
    if (values.hasOwnProperty(key)) {
      return this.escape(values[key]);
    }
    return txt;
  }.bind(this));
};

connection.query("UPDATE posts SET title = :title", { title: "Hello MySQL" });
```
##获取插入值之后的ID
如果你想获取插入一行值之后，获取自动递增主键的ID。你可以这样获取:
```js
connection.query('INSERT INTO posts SET ?', {title: 'test'}, function(err, result) {
  if (err) throw err;

  console.log(result.insertId);
});

```
当处理大数字的时候(超过javascript Number类型的精度),你需要启用`supportBigNumbers`以便把ID作为字符串类型读取。否者会抛出错误.
而且当从数据库中查询的数字是一个`big number`类型的时候，你也需要把`supportBigNumbers`选项设置为`true`，否则查询出来的数据在传输过来的时候由于精度限制，自动删除超出部分。
##获取影响的行数
你可以在执行delete，insert，update之后获取影响的行数
```js
connection.query('DELETE FROM posts WHERE title = "wrong"', function (err, result) {
  if (err) throw err;

  console.log('deleted ' + result.affectedRows + ' rows');
})
```
##获取改变的行数
你可以获取执行update之后改变的行数."changedRows" 与"affectedRows"不同在于,changeRows是获取update之后影响的行数. 
```js
connection.query('UPDATE posts SET ...', function (err, response) {
  if (err) throw err;

  console.log('changed ' + result.changedRows + ' rows');
})
```
##获取连接ID
你可以使用`threadId`方法来获取连接MySQL的ID(线程ID)
```js
connection.connect(function(err) {
  if (err) throw err;
  console.log('connected as id ' + connection.threadId);
});
```
##执行并行查询
MySQL的协议是顺序执行的。所以这就意味这你需要建立多个连接去实现并行查询,你应该需要一个池(Pool)来管理连接。一个简单的方法就是每一个连接都创建的一个HTTP请求连接.
##数据流查询
有时，你可能去执行一个大的查询，并且要处理查询返回的每一行结果。那么你可以尝试这样做：
```js
var query = connection.query('SELECT * FROM posts');
query
  .on('error', function(err) {
    // 处理错误，当出现错误时,会立即发出一个end事件
  })
  .on('fields', function(fields) {
    // the field packets for the rows to follow
  })
  .on('result', function(row) {
   // 处理工程中涉及到I/O可以在这里先暂停连接
    connection.pause();

    processRow(row, function() {
      connection.resume();
    });
  })
  .on('end', function() {
    // 获取所有查询内容
  });
```

在上面的例子中请注意几件事情:
 
*同常的时候你希望当接收到一定数量的查询结果的时候再执行`pause()`方法,这数量取决于你查询总的数量和数据的大小。
*`pause()`/`resume()`操作底层socket和解析器时，可以确定在调用`pause()`方法之后再有`result`事件被执行
*当有多条数据流读取时，不能再给query()方法添加一个回调函数.
在'result'事件中不仅可以返回查询的数据也可以确认query/INSERT执行是否成功.
*除此之外，你应该有兴趣知道当前的模块并不支持单独一行的流读取。它们都是被缓存起来当SQL执行完之后一并把结果返回过来。假如你有在大型的案例中应用到了MySQL的流技术。我很想能够与您分享。

###管道结果（Piping results）和[Streams2](http://blog.nodejs.org/2012/12/20/streams2/)
`query`对象提供了一个非常方便的方法`.stream`(可选).它把查询事件封装成了可读(Readable)的Streams2对象,此流可以很容易地通过管道`downstream`，并提供自动化暂停/恢复，基于`downstream`堵塞和可选`highWaterMark`。该流的`objectMode`参数默认设为`true` 。
例如，把查询结果通过piping导入到另一个流中(最大缓存为5)的简单例子：
```js
connection.query('SELECT * FROM posts')
  .stream({highWaterMark: 5})
  .pipe(...);
```
###多语句查询
出于安全考虑，多语句查询默认是禁用的.(如果值没有经过转义，那么很有可能会导致SQL注入攻击)。如果你想使用此功能，你必须在连接中启用它：
```js
var connection = mysql.createConnection({multipleStatements: true});
```
一旦启用，你就可以执行多条语句查询了。例如：
```js
connection.query('SELECT 1; SELECT 2', function(err, results) {
  if (err) throw err;

  // `results` is an array with one element for every statement in the query:
  console.log(results[0]); // [{1: 1}]
  console.log(results[1]); // [{2: 2}]
});
```
此外，您也可以串行理的多个语句查询的结果：
 
```js
var query = connection.query('SELECT 1; SELECT 2');

query
  .on('fields', function(fields, index) {
    // the fields for the result rows that follow
  })
  .on('result', function(row, index) {
    // index refers to the statement this result belongs to (starts at 0)
  });
```
如果你有一个查询语句出现了错误，那么抛出的错误会包含在`err.index`属性里面并且会告诉你是哪条语句出现了错误。同时当发生错误时对于剩余的查询语句MySQL也会停止执行.
注意：目前利用流来执行多条查询语句的接口还在试验阶段。所以我很期待能够得到您的反馈。
##储存过程
你可以在你的查询语句里面调用MySQL驱动中自带的任何存储过程，如果你使用存储过程生成的多个结果集，其实也就与您使用多语句查询生成得出的结果是一样的。
##合并重叠的字段
当我们使用JOIN函数执行查询的时候得到的结果里面有很多字段是重复的。默认情况下Node-MySQL会按照列读取顺序把一些冲突的列名进行合并。但是这样有可能会导致一些接收到的值变得不可用。
不过，您可以指定在表名中嵌套您需要的列，就像这样： 
```js
var options = {sql: '...', nestTables: true};
connection.query(options, function(err, results) {
  /* results will be an array like this now:
  [{
    table1: {
      fieldA: '...',
      fieldB: '...',
    },
    table2: {
      fieldA: '...',
      fieldB: '...',
    },
  }, ...]
  */
});
```
或者你可以使用字符串分隔符合并成你想要的结果:
 
```js
var options = {sql: '...', nestTables: '_'};
connection.query(options, function(err, results) {
  /* results will be an array like this now:
  [{
    table1_fieldA: '...',
    table1_fieldB: '...',
    table2_fieldA: '...',
    table2_fieldB: '...',
  }, ...]
  */
});
```
##事务处理
在连接层中可以支持简单的事务处理：
```js
connection.beginTransaction(function(err) {
  if (err) { throw err; }
  connection.query('INSERT INTO posts SET title=?', title, function(err, result) {
    if (err) { 
      connection.rollback(function() {
        throw err;
      });
    }

	var log = 'Post ' + result.insertId + ' added';

	connection.query('INSERT INTO log SET data=?', log, function(err, result) {
	  if (err) { 
        connection.rollback(function() {
          throw err;
        });
      }  
	  connection.commit(function(err) {
	    if (err) { 
          connection.rollback(function() {
            throw err;
          });
        }
	    console.log('success!');
	  });
    });
  });
});
```
请注意，执行START TRANSACTION, COMMIT,和 ROLLBACK 这些简单命令的方法分别是transaction(),Commit()和rollback(),了解MySQL中一些会造成隐式提交语句很重要。具体的可以看看MySQL的官方文档[in the MySQL documentation](http://dev.mysql.com/doc/refman/5.5/en/implicit-commit.html)
##错误处理
这个模块包含了错误处理机制，不过在编码的时候你还应该去自己检查自己的代码。看看是否会有一些意想不到的错误。
这个模块中所有的错误都是javascript  [Error][]的对象实例，同时它还有两个属性:
* `err.code`: 任一的MySQL错误 [MySQL server error][] (例如. `'ER_ACCESS_DENIED_ERROR'`), Node.js错误 (例如.`'ECONNREFUSED'`) 或者是内部错误 (e.g. '`PROTOCOL_CONNECTION_LOST'`).
* `err.fatal`:布尔值,这个对象表示是否能够连接到服务器.
[Error]: https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Error
[MySQL server error]: http://dev.mysql.com/doc/refman/5.5/en/error-messages-server.html
致命的错误都可以在回调函数中捕获到。在下面这个例子中,所引起的错误是因为改连接试图连接到一个无效的端口上面。因此错误对象会被传递到回调函数中并且能够使用`err.code`或`err.fatal`知道错误的具体情况:

```js
var connection = require('mysql').createConnection({
  port: 84943, // WRONG PORT
});

connection.connect(function(err) {
  console.log(err.code); // 'ECONNREFUSED'
  console.log(err.fatal); // true
});

connection.query('SELECT 1', function(err) {
  console.log(err.code); // 'ECONNREFUSED'
  console.log(err.fatal); // true
});
```
一般情况下错误是只委托给它所属的回调函数，例如下面这个例子。只有第一个回调函数接收到了错误信息，而第二个同样是按照预期的方式执行的并不会捕获第一个查询的错误：

```js
connection.query('USE name_of_db_that_does_not_exist', function(err, rows) {
  console.log(err.code); // 'ER_BAD_DB_ERROR'
});

connection.query('SELECT 1', function(err, rows) {
  console.log(err); // null
  console.log(rows.length); // 1
});
```
最后值得提醒的是,有时候你可以把错误处理不放在与查询一起的回调函数里面，就如同上面的那个例子。你可以把错误处理放在连接对象上的错误事件里面。就像下面这样：
```js
connection.on('error', function(err) {
  console.log(err.code); // 'ER_BAD_DB_ERROR'
});

connection.query('USE name_of_db_that_does_not_exist');
```
注意:`error`在Node中是一个特殊的对象，如果它没有被挂在一个事件上而是单独出现，那么就很有可能出现堆栈错误并且关闭NodeJS程序进程.
最后：这个模块处理错误的初衷都不是悄悄的处理掉错误，你应该把错误的处理放在回调函数里面。但是如果你不喜欢这么麻烦并且忽略掉错误。那么你可以这样做：
```js
// I am Chuck Norris:
connection.on('error', function() {});
```
##异常安全处理
这个模块的异常处理很安全，也就是说在回调函数中抛出一个错误之后你可以使用’uncaughtException‘或域(domain)去捕获错误，然后继续的去使用做下面的事情。
##类型转换
为了您的使用方面，这个驱动会自动把MySQL中的一些类型转换为原生的javascript的类型。下面列举的是转换的类型：
###Number

* TINYINT
* SMALLINT
* INT
* MEDIUMINT
* YEAR
* FLOAT
* DOUBLE
###Date

* TIMESTAMP
* DATE
* DATETIME
###Buffer

* TINYBLOB
* MEDIUMBLOB
* LONGBLOB
* BLOB
* BINARY
* VARBINARY
* BIT (最后一个字节会使用0来填充)
### String

* CHAR
* VARCHAR
* TINYTEXT
* MEDIUMTEXT
* LONGTEXT
* TEXT
* ENUM
* SET
* DECIMAL (可能会超过float精度)
* BIGINT (可能会超过float精度)
* TIME (转换为日期, but what date would be set?)
* GEOMETRY (从来没有用错，当你使用的时候你可以联系我们)
我们不建议你把类型转换这个参数禁用，但是如果你想禁用也可以在连接的时候就去做（这种方法可能在以后的版本中删除/改变）：
```js
var connection = require('mysql').createConnection({typeCast: false});
```
或者在查询层做：
```js
var options = {sql: '...', typeCast: false};
var query = connection.query(options, function(err, results) {

});
```
你也可以通过一个处理函数来转换自己想要的类型，通过已知的一些字段的信息，像数据库，表名和字段名，数据类型和长度。如果你只想自己定义一个类型转换函数。你可以在查询的回调函数中做。例如你把TINYINT(1)转换为布尔值：
```js
connection.query({
  sql: '...',
  typeCast: function (field, next) {
    if (field.type == 'TINY' && field.length == 1) {
      return (field.string() == '1'); // 1 = true, 0 = false
    }
    return next();
  }
});
```
__警告：你必须使用解析器中内建的三个field函数中的一个，在你自定义的类型转换回调函数中。他们只能调用一次：__
```
field.string()
field.buffer()
field.geometry()
```
或者使用别名：
```
parser.parseLengthCodedString()
parser.parseLengthCodedBuffer()
parser.parseGeometryValue()
```
__如果你需要使用field函数，。你可以在RowDataPacket.prototype._typeCast中找到关于field函数的一些文档资料__

##连接标记
如果,由于某些原因你需要修改默认的连接标记,那么你可能需要使用flags选项。通过在连接配置的选项列表中添加这个选项，那么你就可以修改默认的连接标记.如果你不想使用默认的`flag`你可以使用一个减号来取消掉。或者在连接的配置选项列表里面添加一个flag选项，而不写值，仅仅就是一个flag名字在哪里（不区分大小写）。PS:不像去掉`flag`选项一样,在`flag`的前面加一个`+`号：
**请注意：有些默认的flag目前还不支持（例如：SSL,Compression）。**
例子：
下面的例子是使用黑名单FOUND_ROWS flag例子：
```js
var connection = mysql.createConnection("mysql://localhost/test?flags=-FOUND_ROWS");
```
###默认标记
- LONG_PASSWORD
- FOUND_ROWS
- LONG_FLAG
- CONNECT_WITH_DB
- ODBC
- LOCAL_FILES
- IGNORE_SPACE
- PROTOCOL_41
- IGNORE_SIGPIPE
- TRANSACTIONS
- RESERVED
- SECURE_CONNECTION
- MULTI_RESULTS
- MULTI_STATEMENTS (如果使用` multipleStatements ` 选项就激活)
###其他的可用标记
- NO_SCHEMA
- COMPRESS
- INTERACTIVE
- SSL
- PS_MULTI_RESULTS
- PLUGIN_AUTH
- SSL_VERIFY_SERVER_CERT
- REMEMBER_OPTIONS
##调试与问题查看
如果在运行过程中出现了问题，你可以在连接的配置选项中添加一个`debug`参数来帮助你调试：
```js
var connection = mysql.createConnection({debug: true});
```

它会将输入的信息与输出的信息标准输出的显示出来，你还可以通过把数据包的类型转换成一个数据数组对象来方便调试:
```js
var connection = mysql.createConnection({debug: ['ComQueryPacket', 'RowDataPacket']});
```


限制查询与数据包；
如果没有帮助，你可以打开github的问答社区。一个好的GitHub问题有以下几个特征：
* 提供能够重现该问题的代码（如果可以）
* 尽可能的说清楚您的调试环境（MySQL版本，nodeJS版本，操作系统等等）。

##运行单元测试
设置环境变量`MYSQL_DATABASE`,` MYSQL_HOST`,` MYSQL_PORT`,` MYSQL_USER` 和` MYSQL_PASSWORD`。当你测试的时候你可以需要把这些配置放在一个`config.sh`文件或者是源代码中。然后运行`npm test`。
例如，你安装的MySQL是运行在localhost:3306上面并且没有给root设置密码，那么你可以像下面这样做：
```
mysql -u root -e "CREATE DATABASE IF NOT EXISTS node_mysql_test"
  MYSQL_HOST=localhost MYSQL_PORT=3306 MYSQL_DATABASE=node_mysql_test MYSQL_USER=root MYSQL_PASSWORD= make test
```

##备忘录
* 预查询语句
* 查询时调用 `setTimeout() `方法
* 支持 UTF-8 / ASCII编码

