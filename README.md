# ExBinance

[![Build Status](https://github.com/fremantle-capital/ex_binance/workflows/Test/badge.svg?branch=master)](https://github.com/fremantle-capital/ex_binance/actions?query=workflow%3ATest)
[![Coverage Status](https://coveralls.io/repos/github/fremantle-capital/ex_binance/badge.svg?branch=master)](https://coveralls.io/github/fremantle-capital/ex_binance?branch=master)
[![hex.pm version](https://img.shields.io/hexpm/v/ex_binance.svg?style=flat)](https://hex.pm/packages/ex_binance)

Binance API Client for Elixir

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `binance` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:ex_binance, "~> 0.0.5"}
  ]
end
```

## Setup

_/config.exs_

```elixir
config :ex_binance, domain: "api.binance.com"
```

```elixir
@credentials %ExBinance.Credentials{
    api_key: System.get_env("BINANCE_API_KEY"),
    secret_key: System.get_env("BINANCE_API_SECRET")
  }
```

## Request

```elixir
ExBinance.Private.get_account(@credentials)
```

```elixir
ExBinance.Public.ping()
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/binance](https://hexdocs.pm/binance).
