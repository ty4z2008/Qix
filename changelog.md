## Changelog

Public releases are all root nodes.  
Incremental version bumps that were not released publicly are nested where appropriate.

P.S. If there is a standard (popular) changelog format, please let me know.

- **0.3.0 : 2013.02.24**
    - **Features**
    - Update twitter bootstrap to 2.2.2. Add responsiveness and update design a bit.
    - @techotaku fixes custom tagline support (finally made it in!)
    - @opie4624 adds ability to set tags from the command-line.
    - @lax adds support for RSS feed. Adds rss and atom html links for discovery.
    - Small typo fixes.

    - **Bug Fixes**
    - @xuhdev fixes theme:install bug which does not overwrite theme even if saying 'yes'.

- **0.2.13 : 2012.03.24**   
    - **Features**
    - 0.2.13 : @mjpieters Updates pages_list helper to only show pages having a title.
    - 0.2.12 : @sway recommends showing page tagline only if tagline is set.
    - 0.2.11 : @LukasKnuth adds 'description' meta-data field to post/page scaffold.

    - **Bug Fixes**
    - 0.2.10 : @koriroys fixes typo in atom feed

- **0.2.9 : 2012.03.01**   
    - **Bug Fixes**
    - 0.2.9 : @alishutc Fixes the error on post creation if date was not specified.

- **0.2.8 : 2012.03.01**   
    - **Features**
    - 0.2.8 : @metalelf0 Added option to specify a custom date when creating post.
    - 0.2.7 : @daz Updates twitter theme framework to use 2.x while still maintaining core layout. #50
              @philips and @treggats add support for page.tagline metadata. #31 & #48
    - 0.2.6 : @koomar Adds Mixpanel analytics provider. #49
    - 0.2.5 : @nolith Adds ability to load custom rake scripts. #33
    - 0.2.4 : @tommyblue Updated disqus comments provider to be compatible with posts imported from Wordpress. #47

    - **Bug Fixes**
    - 0.2.3 : @3martini Adds Windows MSYS Support and error checks for git system calls. #40
    - 0.2.2 : @sstar Resolved an issue preventing disabling comments for individual pages #44
    - 0.2.1 : Resolve incorrect HOME\_PATH/BASE\_PATH settings

- **0.2.0 : 2012.02.01**   
  Features
    - Add Theme Packages v 0.1.0
      All themes should be tracked and maintained outside of JB core.
      Themes get "installed" via the Theme Installer.
      Theme Packages versioning is done separately from JB core with
      the main intent being to make sure theme versions are compatible with the given installer.

    - 0.1.2 : @jamesFleeting adds facebook comments support
    - 0.1.1 : @SegFaultAX adds tagline as site-wide configuration

- **0.1.0 : 2012.01.24**   
  First major versioned release.   
  Features   
    - Standardize Public API
    - Use name-spacing and modulation where possible.
    - Ability to override public methods with custom code.
    - Publish the theme API.
    - Ship with comments, analytics integration.
  
- **0.0.1 : 2011.12.30**    
  First public release, lots of updates =p
  Thank you everybody for dealing with the fast changes and helping
  me work out the API to a manageable state.
  
