# Noir library by Wagmi Labs*

A public Noir library repo containing a specific Noir functions we've implemented and we're using in our apps: __Proof of Proximity__.

## Example

An example of how to use the Proof of Proper Secret functions such as `proof_of_proximity::check_points_proximity` is available in `./example/`.

## Using the library

1. Add the library to your Noir project dependencies in the `Nargo.toml` file.

```toml
[dependencies]
proof_of_proximity = {tag = "v1.0.0", git = "https://github.com/fruity-labs/proof-of-proximity"}
```

2. Import the library and function into your Noir code.

Partial example (for a fully exhaustive one, see in `./example/`):
```rust
use dep::std;
use dep::proof_of_proximity;

fn main(){
    // ...
    let pointA = proof_of_proximity::coordinates_to_point(latitudeA, longitudeA, 0);
    let pointB = proof_of_proximity::coordinates_to_point(latitudeB, longitudeB, 0);
    proof_of_proximity::check_points_proximity(commitmentA, commitmentB, pointA, pointB, distance_threshold);
    std::println("They're close enough!");
    // ...
}
```
## Thanks

Credit to [@critesjosh](https://github.com/critesjosh) for [the public Noir library demo](https://github.com/critesjosh/noir-lib-demo).
And cheers to [@signorecello](https://github.com/signorecello) for his guidance and review.

--

**(Wagmi Labs == [@madztheo](https://github.com/madztheo) & [@guelowrd](https://github.com/guelowrd), creators of [Fruity Friends](https://github.com/madztheo/zk-fruits-front-end))*