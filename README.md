# website
Hope's Horse Therapy Website

To build locally, run `bundle install` followed by `bundle exec jekyll build`.
For a local preview, run `bundle exec jekyll serve`.

The Gemfile lists Jekyll and the plugins configured in `_config.yml` directly.
The site uses local layouts and includes, so it does not need `jekyll-remote-theme`
or the `github-pages` gem bundle. GitHub Pages 232 pins the remote-theme plugin
to a version that requires vulnerable rubyzip 2.x; omitting those unused dependencies
removes rubyzip from the local build. The Jekyll version remains 3.10.0 to match
the GitHub Pages build environment.
