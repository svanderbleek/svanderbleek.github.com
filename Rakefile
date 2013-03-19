def post_format
  "#{Time.now.utc.strftime("%Y-%m-%d")}-#{ENV['title']}.html"
end

file :post do |t|
  File.open("_posts/#{post_format}", 'w+') do |file|
    file << <<-TEMPLATE.gsub(/^\s*/, '')
    ---
    layout: post

    title: #{ENV['title']}
    ---
    TEMPLATE
  end
end
