# Tarso

Tarso is a library datapack containing general mathematical utilities for score calculations **without** using macro functions.

## Usage

### Calculation

To calculation, put the score in `math.target` and (maybe) `math.source`, then call operations, the score returned will be presented in `math.target`.

| Operation | Function | General Expression | Desciption |
| --- | --- | --- | --- |
| Left Shift | `math:ls` | `math.target = math.target >> math.source` |  |
| Right Shift | `math:rs` | `math.target = math.target << math.source` |  |
| Addition | `math:add` | `math.target = math.target + math.source` |  |
| Multiplication | `math:mul` | `math.target = math.target * math.source` |  |
| Power | `math:pow` | `math.target = math.target ^ math.source` |  |
| Subtraction | `math:sub` | `math.target = math.target - math.source` |  |
| Division | `math:div` | `math.target = math.target / math.source` |  |
| Logarithm | `math:log` | `math.target = log math.source (math.target)` |  |
| Common Logarithm | `math:lg` | `math.target = log 10 (math.target)` |  |
| Natural Logarithm | `math:ln` | `math.target = log 2 (math.target)` |  |
| Square Root | `math:sqrt` | `math.target = sqrt(math.target)` |  |
| Modulus | `math:mod` | `math.target = math.target % math.source` |  |
| Remainder | `math:rem` | `math.target = math.target % math.source` |  |
| Negativity | `math:neg` | `math.target = -math.target` |  |
| Absolutation | `math:abs` | `math.target = (math.target < 0) ? -math.target : math.target` |  |
| Sign | `math:sig` | `math.target = math.target / (math.target < 0) ? -math.target : math.target` |  |
| Factorial | `math:fact` | `math.target = math.target!` |  |
| Permutation | `math:perm` | `math.target = P(math.target, math.source)` |  |
| Combination | `math:comb` | `math.target = C(math.target, math.source)` |  |
| Hypot | `math:hyp` |`math.target = sqrt(**math.target + **math.source)` |  |
| Vector | `math:vec` | `math.x = CORDIC(math.target).x` `math.y = CORDIC(math.target).y` | Precision is controled by `math.source`. |
| Tangent | `math:tan` | `math.target = tan(math.target)` | Precision is controled by `math.source`. |
| Cotangent | `math:cot` | `math.target = cot(math.target)` | Precision is controled by `math.source`. |
| Sine | `math:sin` | `math.target = sin(math.target)` | Precision is controled by `math.source`. |
| Cosine | `math:cos` | `math.target = cos(math.target)` | Precision is controled by `math.source`. |

### The Stack

Tarso comes with a stack of 16 sorts. To transfer scores, put the score in `math.buffer` before pushing and the score poped out will be presented in `math.buffer`.

| Operation | Function |
| --- | --- |
| Push | `math:push` |
| Pop | `math:pop` |
| Seek | `math:seek` |

## Notes

1. Objectives other than those belong to the stack can be overwritten during calculations.

2. Pushing a score into the stack while it's full make no sense.

## FAQ

### 1. Why is the natural logarithm inaccurate?

It cannot be fixed except using large-number calculation, which is extremely slow. Currently it has a base of 2.
