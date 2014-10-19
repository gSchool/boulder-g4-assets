desc "create a new class notes file"
task :day do
  require 'active_support/core_ext/integer/inflections'
  require 'date'
  last_day = Dir.glob('class-notes/*.md').last
  date_string = File.basename(last_day).sub('class-notes-', '').sub('.md', '')
  date = Date.new(*date_string.split('-').map(&:to_i))
  next_date = date.next_day
  until next_date.saturday? == false && next_date.sunday? == false
    next_date = next_date.next_day
  end
  new_path_name = next_date.strftime("class-notes/class-notes-%Y-%m-%d.md")
  File.open(new_path_name, "w")
end
