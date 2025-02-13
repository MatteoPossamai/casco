# Spectre Variants

For this project we start with the following Spectre variants:

## Spectre v1

Also called PHT(Pattern History Table) or B, uses miss prediction over branch instructions and uses caches as side channel.

### Snippet example

```c
void victim_function(size_t x) {
    if (x < array_size) {
        uint8_t secret = array[x];
        uint8_t temp = probe[secret * 4096];
    }
}
```

### Contract

TODO

## Spectre v4

Also called STL (Store To Load), or S, uses the store buffer to speculate on the value of loads on a non yet committed store, that might be overwritten in the meanwhile.

### Snippet example

```c
void victim_function() {
    global_var = secret;
    uint8_t leaked = temp_array[global_var * 4096];
}
```

### Contract

TODO
