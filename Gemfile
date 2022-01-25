# frozen_string_literal: true

source 'https://rubygems.org'

# Look in asciidoctor-pdf.gemspec for runtime and development dependencies
gemspec

gem 'asciidoctor', ENV['ASCIIDOCTOR_VERSION'], require: false if ENV.key? 'ASCIIDOCTOR_VERSION'
gem 'matrix' if (Gem::Version.new RUBY_VERSION) >= (Gem::Version.new '3.1.0')
gem 'open-uri-cached', '~> 1.0.0', require: false
gem 'pdf-reader', '2.8.0', require: false
gem 'prawn-gmagick', ENV['PRAWN_GMAGICK_VERSION'], require: false if ENV.key? 'PRAWN_GMAGICK_VERSION'
# NOTE: use prawn-table from upstream (pre-0.2.3) to verify fix for #599
gem 'prawn-table', git: 'https://github.com/prawnpdf/prawn-table', ref: '515f2db294866a343b05d15f94e5fb417a32f6ff', require: false
gem 'pygments.rb', ENV['PYGMENTS_VERSION'], require: false if ENV.key? 'PYGMENTS_VERSION'
gem 'rexml', require: false if (Gem::Version.new RUBY_VERSION) >= (Gem::Version.new '3.0.0')
gem 'rghost', ENV['RGHOST_VERSION'], require: false if ENV.key? 'RGHOST_VERSION'
gem 'rouge', ENV['ROUGE_VERSION'], require: false if ENV.key? 'ROUGE_VERSION'
gem 'text-hyphen', require: false

group :docs do
  gem 'yard', require: false
end

group :lint do
  gem 'rubocop', '~> 1.14.0', require: false
  gem 'rubocop-rake', '~> 0.5.0', require: false
  gem 'rubocop-rspec', '~> 2.3.0', require: false
end

group :coverage do
  gem 'deep-cover-core', '~> 1.1.0', require: false
  gem 'simplecov', '~> 0.21.0', require: false
end
