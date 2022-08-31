# Json File Parser

A CLI to parse json files, being able to output properties and array indexes
  

## 1. Instalation
### 1.1 Cargo

    cargo install jfp

### 1.2 Ready-to-use executable

|OS|Architecture| File*|
|--|--|--|
|Linux|x86_64|[jfp](https://github.com/costa86/jfp/blob/master/jfp)|
|Windows|x86_64|[jfp.exe](https://github.com/costa86/jfp/blob/master/jfp.exe)|

    ./jfp


## 2. Usage

    Lorenzo Costa <http://www.costa86.tech>
    Json File Parser

    USAGE:
        jfp --filename <FILE> --keys <TEXT>

    OPTIONS:
        -f, --filename <FILE>    Json file to parse
        -h, --help               Print help information
        -k, --keys <TEXT>        Property to search for. Use '.' for nested properties and/or array
                                indexes
        -V, --version            Print version information


## 3. Example

[the-lord-of-the-rings.json](/examples/the-lord-of-the-rings.json)
```json

{
    "title": "the lord of the rings",
    "characters": [
        {
            "name": "frodo",
            "race": "hobbit"
        },
        {
            "name": "aragorn",
            "race": "human"
        }
    ]
}

```

```sh
./jfp -f ./examples/the-lord-of-the-rings.json -k title 
```

```json
"the lord of the rings"
```

```sh
./jfp -f ./examples/the-lord-of-the-rings.json -k characters.0.race
```

```json
"hobbit"
```
