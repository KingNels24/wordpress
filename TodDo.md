## Website

- [x] add .htaccess
- [x] add robots.txt
- [x] Travis CI integration
- [x] Fix design
- [ ] add missing Support page
- [ ] fix Contact page
- [ ] fix About page
- [ ] automatically hide 'Pinned Posts' (_maybe_)
- [ ] expand pictures when clicking on them (_maybe_)
- [x] fix Hungarian language (add more languages)
- [ ] change font(s) (?)
- [ ] review Google settings (_already did but there some privacy questions left_)
- [ ] add more mobile devices + detections + fallbacks
- [x] load fonts locally as fallback
- [ ] add page status in 'About' to check if page is online/offline (low-prio)
    - [ ] Component selector navigation (low-prio)
    - [ ] add video frames (low-prio)
- [ ] ...

## Website Features
- [ ] [jQuery Smooth Scroll](https://github.com/kswedberg/jquery-smooth-scroll)
- [ ] add [Lazyload](https://github.com/aFarkas/lazysizes) support
- [ ] add Support for threaded/nested comments
- [ ] randomize Header image on the FP
- [ ] Improve page performance with [Gulp](http://savaslabs.com/2016/10/19/optimizing-jekyll-with-gulp.html)
- [ ] add [picture tag](https://github.com/robwierzbowski/jekyll-picture-tag)
- [ ] add [WuFoo](https://www.wufoo.com/) + (or) [Mailgun](https://www.mailgun.com) for eMail support questions


## Plugin related 

#### Mailchimp

- [ ] fix header image 
- [ ] review (again) privacy policy
- [ ] adjust reCAPTCHA v2 image(s)
- [ ] ...


#### Upscri.be Newsletter

- [ ] change 'Sign up' button color and size (_maybe_)
- [ ] change font? anti-aliasing correction for some Browsers
- [ ] possible hide some 'Newsletter' popups on certain pages (_maybe_)
- [ ] ...


## Blog structure

├── gulp                      # => gulp tasks
├── src                       # => source Jekyll files and assets
|  ├── _includes
|  ├── _layouts
|  ├── _plugins
|  ├── ...
|  ├── _posts
|  ├── assets
|  |  ├── icons
|  |  ├── images
|  |  |   └── feature
|  |  ├── javascript
|  |  |   ├── plugins
|  |  |   ├── vendor
|  |  |   └── main.js
|  |  ├── stylesheets
|  |  |   ├── vendor
|  |  |   ├── ...
|  |  |   └── style.scss
├── .editorconfig
├── .gitignore
├── .htaccess
├── _config.dev.yml
├── _config.yml
├── Gemfile
├── robots.txt
├── #
├── ...