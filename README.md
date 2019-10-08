# bson

LibBSON wrapper for Crystal

## Installation

1. Add the dependency to your `shard.yml`:

   ```yaml
   dependencies:
     bson:
       github: washu/bson.cr
   ```

2. Run `shards install`

## Usage

```crystal
require "bson"
```


example creation of a bson document
```crystal

query = [
    {"$match" => {"status" => "A"}},
    {"$group" => {"_id" => "$cust_id", "total" => {"$sum" => "$amount"}}}]
bson_query = query.to_bson
```

....
you now have a valid bson object to use.

## Development


## Contributing

1. Fork it (<https://github.com/washu/bson.cr/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## Contributors

- [Sal Scotto](https://github.com/washu) - creator and maintainer
