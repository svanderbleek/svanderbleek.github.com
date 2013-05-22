def post_format
  "#{Time.now.utc.strftime("%Y-%m-%d")}-#{ENV['title']}.html"
end

def title_format
  ENV['title'].split('-').map(&:capitalize).join(' ')
end

file :post do |t|
  File.open("_posts/#{post_format}", 'w+') do |file|
    file << <<-TEMPLATE.gsub(/^\s*/, '')
    ---
    layout: post

    title: #{title_format}
    ---
    TEMPLATE
  end
end
