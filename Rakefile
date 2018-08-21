task default: %w(setup)

desc 'Run setup steps'
task :setup do
  sh 'pipenv install --three'
  sh 'bundle install'
end

desc 'Conver to rst'
task :convert, [:filename] do |_task, args|
  sh("pandoc -V mainfont='SimSun' -f markdown -t rst "\
    "source/#{args['filename']}.md -o source/#{args['filename']}.rst")
end
