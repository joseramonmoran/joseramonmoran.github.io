source 'https://rubygems.org'

# Built by the GitHub Actions workflow in .github/workflows/pages.yml, not by
# GitHub's built-in Pages builder, so we control the Jekyll version here.
# Academic Pages targets Jekyll 4.
gem 'jekyll', '~> 4.3'
# Jekyll 4.4 ships jekyll-sass-converter 3 (dart-sass), which rejects the
# libsass-era Susy/Breakpoint stylesheets this theme vendors. Stay on 2.x.
gem 'jekyll-sass-converter', '~> 2.2'

group :jekyll_plugins do
  gem 'jekyll-feed'
  gem 'jekyll-gist'
  gem 'jekyll-paginate'
  gem 'jekyll-sitemap'
  gem 'jekyll-redirect-from'
  gem 'jemoji'
end

gem 'webrick', '~> 1.8'

# Removed from Ruby's standard library in 3.4; Jekyll's dependencies still want them.
gem 'base64'
gem 'bigdecimal'
gem 'csv'
gem 'logger'
