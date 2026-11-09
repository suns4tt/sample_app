guard :minitest, cli: "bin/rails test", all_on_start: false do  
  watch('config/routes.rb') { 'test/controllers' }

  watch('test/test_helper.rb') { 'test' }

  watch(%r{^app/controllers/(.*)_controller\.rb$}) do |matches|
    "test/controllers/#{matches[1]}_controller_test.rb"
  end

  watch(%r{^app/views/(.+)/(.+)\.html\.erb$}) do |matches|
    "test/controllers/#{matches[1]}_controller_test.rb"
  end

  watch(%r{^test/controllers/(.*)_test\.rb$})
  
end