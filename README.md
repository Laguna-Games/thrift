This is a mirror of Apache's Thrift library for Erlang.

We mirror releases from `apache/thrift` by using `git filter-branch`.

```sh
export TAG=v0.16.0
git clone https://github.com/apache/thrift.git --branch $TAG --depth 1
cd thrift
git subtree split --prefix=lib/erl/ --branch=mirror
git remote add mirror git@github.com:Laguna-Games/thrift.git
git push -f mirror refs/heads/mirror:refs/tags/$TAG
```

This can be used via Hex:

```elixir
{:thrift, github: "Laguna-Games/thrift", tag: "v0.16.0"}
```
