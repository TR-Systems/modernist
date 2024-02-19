source "https://rubygems.org"

gem "github-pages", "~> 231", group: :jekyll_plugins

# Jekyll-feed is for Atom blog
# group :jekyll_plugins do
#   gem "jekyll-feed", "~> 0.12"
# end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# IS THIS NEEDED??? I doubt it
# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# IS THIS NEEDED??? I wonder
# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# This IS needed
gem "webrick", "~> 1.8"
