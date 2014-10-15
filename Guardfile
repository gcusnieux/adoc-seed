require 'asciidoctor'
require 'erb'

guard 'shell' do
  watch(/^adoc\/.+\.adoc$/) {|m|
    Asciidoctor.render_file(m[0], :to_dir => "html/", :safe => Asciidoctor::SafeMode::UNSAFE)
  }
end

guard 'livereload' do
  watch(%r{^html\/.+\.(css|js|html)$})
end