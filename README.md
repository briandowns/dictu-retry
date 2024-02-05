# retry 

retry is a module for running [Dictu](https://github.com/) functions that may fail but need to be ran again without intervention. The caller can optionally specify an exponential backoff value.

## Installation

```sh
dictum install github.com/briandowns/dictu-retry
```

## Examples

```cs
retry(func, 5).match(
    def(result)=> {
        print(result);
    },
    def(error) => {
        print(error);
        System.exit(1);
    }
);
```

```cs
retry(func, 5, 1).match(
    def(result)=> {
        print(result);
    },
    def(error) => {
        print(error);
        System.exit(1);
    }
);
```

## Contact

Brian Downs [@bdowns328](http://twitter.com/bdowns328)

## License

Kahless source code is available under the BSD 3 Clause [License](/LICENSE).
