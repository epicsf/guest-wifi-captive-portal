desc 'Publish site to S3'
task :deploy do
  puts "Publishing site"
  sh %Q{
    s3cmd sync public/ s3://epic-guest-wifi-captive-portal/ \
      --config .s3cfg \
      --cf-invalidate \
      --delete-removed \
      --acl-public \
      --verbose \
  }
end
