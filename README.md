Command line utility to interact with RIAK distributed database

### What can I do with this ?

* List all the buckets available in a given RIAK instance
* List all keys in a given bucket
* Read an object given a key under a given bucket
* Create or update an object for a given key
* Delete riak objects and buckets
* Tabbing gives you auto complete support for sub commands
* More to come..

### How do I use this ?

Here you go !!

```
Usage:

  riakcli list buckets [bucket-type]                                   -> Lists all the buckets available in RIAK
  riakcli list keys [bucket-type] [bucket-name]                        -> Lists all keys in a given bucket

  riakcli get object [bucket-type] [bucket-name] [key]                 -> Gets the object associated with a given key in a specified bucket
  riakcli put object [bucket-type] [bucket-name] [key] [object-json]   -> Creates/Updates an object for a given key in a specified bucket
  riakcli search by_index [bucket-type] [bucket-name] [index-name] [index-value]
                                                                       -> Searches given value by secondary index in a specified bucket
  riakcli search by_yz [index-name] [query]
                                                                       -> Searches by yokozuna
  riakcli delete bucket [bucket-type] [bucket-name]                    -> Deletes all objects in a specified bucket
  riakcli delete object [bucket-type] [bucket-name] [key]              -> Deletes an object in a given bucket
  riakcli flush [bucket-type]                                          -> Deletes all the buckets in RIAK
  riakcli create search_index [index-name] (n_val)                     -> Create a search index
  riakcli assign search_index [bucket-type] [bucket-name] [index-name] -> Assign a bucket to a search index

  riakcli ping                                           -> Connects to RIAK instance for status
  riakcli help                                           -> Displays this usage information
```

### How do I get started ?

```bash
git clone https://github.com/mtakahashi-ivi/riakcli.git
cd riakcli      
./install.sh      ## After installation, source the riakcli_bashcompletion script as mentioned in installation logs
```

> __After setting it up, riakcli is available @ /usr/local/bin/riakcli (make sure it is added to your PATH)__

### Configuration

By default, this tool connects to RIAK @ __http://localhost:8098__. 
If you want to connect to RIAK on other machine, edit __~/.riakclirc__ and change the appropriate configuration.

Please note __~/.riakclirc__ is created by installation script automatically.

### Whats coming later ?

* Support for HTTPS
* Support for authentication enabled RIAK
* Support for updating objects with headers

### Latest release

`v0.3`


### License

Copyright 2013 Srivatsa Katta

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.



