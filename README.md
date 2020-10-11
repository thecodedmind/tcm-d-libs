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
just a clean API for checking if a string contains a substring
```d
"this is a test string".contains("test"); // returns true
```

## arrayplus
same as strplus.contains
```d
["this", "is", "a", "test"].contains("test"); // returns true
```

## randplus
```d
int i = rand(10); //returns random number between 0 and 10
int r = randrange(10, 100); // returns random number between 10 and 100
```

## colours
Simple class for terminal colours. (Linux)
The API is;

  .*colour*
  .bright_*colour*
  .bg_*colour*
  .bg_bright_*colour*
  .bold
  .underline
  .reversed
  .reset
  .fg(colour_id)
  .bg(colour_id)

Examples:
```d
auto c = new Colours();
writeln(c.red~"This text is red when it prints!"~c.reset); //reset clears all formatting
writeln(c.fg(125)~"Also takes a colour ID, for fg for foreground, fg for background"~c.reset); 
```
