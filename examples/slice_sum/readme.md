# Computes the sum of a slice of floating-point numbers

This example show-cases the performance difference of computing the sum of a
`&[f32]` slice using horizontal or vertical operations. 

To run it:

```
RUSTFLAGS="-C target-cpu=native" cargo run --release
```

On my machine it prints:

```
std::iter::sum: 758 ms
rayon::sum: 67 ms
vertical: 214 ms
horizontal: 291 ms
vertical_par: 60 ms
```
