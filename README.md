# Exploring Stylus

https://docs.arbitrum.io/stylus/gentle-introduction


## Notes

- Stylus lets you write smart contracts in programming languages that compile to WASM, such as Rust, C, C++, and many others, allowing you to tap into their ecosystem of libraries and tools. Rich language and tooling support already exist for Rust. You can try the SDK and CLI with the quickstart.

- Solidity contracts and Stylus contracts are fully interoperable. In Solidity, you can call a Rust program and vice versa, thanks to a second, coequal WASM virtual machine.

- Stylus contracts offer significantly faster execution and lower gas fees for memory and compute-intensive operations, thanks to the superior efficiency of WASM programs.

- Stylus is an upgrade to Arbitrum Nitro (ArbOS 32), the tech stack powering Arbitrum One, Arbitrum Nova, and Arbitrum chains.

## Instructions

### With local install

Requirements : Rust >= 1.81.0, cargo-stylus 0.6.1, Docker, Foundry's cast, git

Have a dev node running

```bash
git clone https://github.com/OffchainLabs/nitro-devnode.git
```

```bash
cd nitro-devnode
```

```bash
./run-dev-node.sh
```

Install the stylus toolchain

```bash
cargo install --force cargo-stylus cargo-stylus-check
```

Add the `wasm32-unknown-unknown` build target to your Rust compiler:

```
rustup target add wasm32-unknown-unknown
```

Run the check

```bash
cargo stylus check
```

