# hxdmp

Generate a hexdump from a byte slice onto a given writer

## Usage
```
let some_bytes = b"Hello, World! I'm hexy";
let mut buffer = Vec::new();
assert!(hexdump(some_bytes, &mut buffer).is_ok());
assert_eq!(
    r#"0000: 48 65 6C 6C 6F 2C 20 57 6F 72 6C 64 21 20 49 27  Hello,.World!.I'
0016: 6D 20 68 65 78 79                                m.hexy"#,
    String::from_utf8_lossy(&buffer)
);
```

## Example Output
```
0000: 48 65 6C 6C 6F 2C 20 57 6F 72 6C 64 21 20 49 27  Hello,.World!.I'
0016: 6D 20 68 65 78 79                                m.hexy
```