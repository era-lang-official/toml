# Era TOML (`github.com/era-lang-official/toml`)

Native TOML configuration file parser and serializer for Era.

## Features
- **Parsing**: Parses standard section tables `[table]` and key-value pairs (strings, integers, booleans).
- **Serialization**: `TomlDoc::stringify()` converts structured config to valid TOML.
- **Typed Lookups**: `get_str`, `get_int`, `get_bool`.

## Usage
```era
import "github.com/era-lang-official/toml";

fn main() {
    let doc = parse_toml("[server]\nport = 8080\n".to_string()).unwrap();
    let port = doc.get_int("server".to_string(), "port".to_string()).unwrap();
}
```

