task :default => :all

desc "Upload to burkelibbey.org"
task :upload do
  system("scp burke_libbey.pdf og:b/files")
end

desc "Commit to git repo"
task :commit do
  system("git add .; git commit -a -m 'Rake auto-commit'")
end

desc "Build PDF"
task :build do
  system("pdflatex burke_libbey.tex")
end

task :all => [:build, :commit, :upload]
