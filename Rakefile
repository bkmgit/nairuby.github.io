#!/usr/bin/env ruby

require 'html-proofer'

task :test do
  puts "\n## Generating Site with Jekyll"
  system "bundle exec jekyll build"

  puts "\n## HTML Proofing the generated site"
  HTMLProofer.check_directory('./_site', alt_ignore: [/.*/]).run
end

task "assets:precompile" do
  exec("jekyll build")
end
