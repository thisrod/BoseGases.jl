# BoseGases.jl

BECs and order parameters.

## Types

```
BoseGas(V, g, N, μ, Ω, ψ₀, nnc)
```
Unit scaling?  Should have ω_perp=1 for V=r².

Specification can be extended or overridden with e.g. `BoseGas(system; nnc=whatever)`.

Constructor `BoseGas(::Grid; g, N)` for untrapped gas.

```
oprm!(system::BoseGas; numerical options)
```
Extend with ψ₀.  Exactly one of μ or N must be specified, the other is set.  Self-consistent with nnc.

Functions for Hamiltonians, angular momentum and so on.  These return `DiffEqOperator`s that act on a `Field`.