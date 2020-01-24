## Count occurences of arbitrary objects

```ruby
arr = [:a, 'tacos', 13e-6, File, :a, :a, File]

counts = Hash.new(0)
arr.each {|element| counts[element] += 1 }
counts

# or

counts = arr.inject(Hash.new(0)) do |hash, value|
  hash[value] += 1
  hash
end

# => {:a=>3, "tacos"=>1, 1.3e-05=>1, File=>2}
```
