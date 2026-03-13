# Gemfile for Jekyll portfolio site on GitHub Pages
source "https://rubygems.org"

# Jekyll version
gem "jekyll", "~> 4.3.0"

# GitHub Pages gem (includes Jekyll)
gem "github-pages", group: :jekyll_plugins

# Default theme
gem "minima", "~> 2.5"

# プラグイン
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows用のgemたち
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1" if Gem.win_platform?

# Lock Jekyll versions for compatibility
gem "jekyll-sass-converter", "~> 2.0"