# From: https://github.com/tatey/tatey.com/blob/master/Rakefile
# run with 'rake deploy' command

task :default => :server
 
desc 'Build site with Jekyll'
task :build do
  jekyll
end
 
desc 'Build and start server with --auto'
task :server do
  jekyll '--server --auto'
end

desc 'Build and deploy'
task :deploy => :build do
  sh 'rsync -rtz --progress --delete _site/ scottwei@scottweisman.com:~/public_html/scottweisman.com'
end

def jekyll(opts = '')
  sh 'rm -rf _site'
  sh 'jekyll ' + opts
end