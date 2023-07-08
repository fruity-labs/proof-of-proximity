# Noir library by Wagmi Labs*

A public Noir library repo containing a specific Noir functions we've implemented and we're using in our apps: __Proof of Proximity__.

## Using the library

1. Add the library to your Noir project dependencies in the `Nargo.toml` file.

```toml
[dependencies]
proof-of-proximity = {tag = "v1.0.0", git = "https://github.com/fruity-labs/proof-of-proximity"}
```

2. Import the library and function into your Noir code.

Example:
```rust
use dep::std;
use dep::proof-of-proximity;

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