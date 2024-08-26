# What I Learn
<details>
<summary><b>Rust:</b></summary></br>

Progress BAR:
<progress value="50" min="0" max="100"></progress>

- [ ] Rust
   - [x] Own Functions
   - [x] Modules
   - [ ] Fancy Apps
   - [ ] More...

<abbr title="My/Example Code - H3"><h3>Example Code</h3></abbr>
<abbr title="This Code 🧑‍💻">

```rs
pub mod modules {
    pub mod math;
    pub mod ask;
    pub mod convert;
}

fn main() {

    println!("{}", modules::math::pow(modules::ask::ask32(), 2));

    if modules::ask::ask32() == modules::math::random(1, 10) {
        println!("Good")
    } else {
        println!("Bad")
    }
    println!("{}", modules::convert::num(modules::ask::askstr()))
}
      
```

</abbr>

### Start Easy: 
Modules:

```rs
pub mod modules {
    pub mod math;
    pub mod ask;
    pub mod convert;
}
```

In folder [`./src/modules`](./src/modules/) are files: [`math.rs`](./src/modules/math.rs), [`ask.rs`](./src/modules/ask.rs), [`covert.rs`](./src/modules/convert.rs), that's why `pub mod modules {...}`.

 - Pub - Public (PL: Publiczny),
 - Mod - Module (PL: Moduł),
 - Modules - Modules (PL: Moduły, nazwa folderu).

This merges into: Public Module `Modules`

Alr, what mean:

```rs
pub mod math;
pub mod ask;
pub mod convert;
```

- Pub - Public (Public, because our "parent" is public and is a folder. If there was no `pub`, you would have to write e.g. `use modules::math::function` for all functions)
- Mod - Module (Now files are our modules 😀)
- [math, ask, convert] - file name in `file explorer`: name.rs


I almost forgot.
Exactly "in `file explorer`: name.rs": 
Example Project Structure:

 __ Project
</br>
 | src
</br>
 |-- modules
</br>
 |-- -- ask.rs
</br>
 |-- -- convert.rs
</br>
 |-- -- math.rs
</br>
 |-- main.rs
</br>
 | ...

### Okay, rest of code

```rs
fn main() {

    println!("{}", modules::math::pow(modules::ask::ask32(), 2));

    if modules::ask::ask32() == modules::math::random(1, 10) {
        println!("Good")
    } else {
        println!("Bad")
    }
    println!("{}", modules::convert::num(modules::ask::askstr()))
}
```
### Let's start with the built-in functions:

```println!("text")``` - print immediately with a new line "text"

Okay, what does e.g. `modules::ask::ask32()` mean - use the `ask32()` command from [ask.rs](./src/modules/ask.rs) from [modules/](./src/modules/)


### Now the functions from our modules:
`modules::math::random(1, 10)` - pick a number from 1 to 10

Math.rs:
```rs
use rand::Rng;

pub fn pow(a: i32, b: i32) -> i32 {
    let mut result = 1;

    for _ in 0..b { 
        result *= a;
    }

    result // return-friendly :)
}

pub fn random(from:i32, to:i32) -> i32 {
    let mut random = rand::thread_rng();
    let random_number: i32 = random.gen_range(from..=to);

    random_number
}
```

### Now try write our own code
1. Go to [Rust Page](https://www.rust-lang.org/learn/get-started),

2. Download Rust Installer,

3. Setup Rust,

4. Open your IDE (vsc, idea),

5. In terminal write: `cargo new project_name`, `cd project_name`

If you want to run your project i recomendeed a plugin in vsc `rust-analyzer` but, you can do this too by writing in terminal: `cargo build` then `cargo run`

</details>

<details>
<summary><b>PREPARED FOR THE NEXT POST</b></summary></br>
- [ ]PREPARED FOR THE NEXT POST

- [x]PREPARED FOR THE NEXT POST

1. PREPARED FOR THE NEXT POST

2. PREPARED FOR THE NEXT POST

</details>
