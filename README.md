# tcm-d-libs
Collection of in-progress utilities for D-lang. (WIP)

## opthandler
```d
import std.stdio, std.regex, std.algorithm, tcm.opthandler;

void main(string[] argv){
  auto opts = new Opt(argv);
  writeln(opts.command());
  writeln(opts.command(1));
  writeln(opts.value("file"));
  writeln(opts.flag("debug"));
}

```
Outputs: 
```
./app --debug writeln bork --file:me
writeln
bork
me
true
```

## strplus
```d
"this is a test string".contains("test"); // returns true
```

## arrayplus
```d
["this", "is", "a", "test"].contains("test"); // returns true
```
