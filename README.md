# genetic-cyber-fuzz
This repository is a future plan:

## Fuzzing FFMPEG
> We will fuzz ffmpeg with afl++ in order to test the genetic fuzzing algorithm, which mutates input accordingly to code coverage (it insert calls to `__afl_maybe_log` in the compiling phase in order to track how the code is behaving according to input).
> AFL generates code coverage output based on modifications in the resulting binary, these modifications log any branches taken accordingly to input mutations (for determinisc algorithms), this data is gathered by the end of each fuzz attempt in order to cover more attack surface.

### Goals:
1. Find a buffer overflow
2. Find a memory disclosure vulnerability
3. Help the open source community to develop a more sofisticated and secure sofrware

### Paths to take
- [ ] Build ffmpeg with AFL
- [ ] Understand what is being fuzzed and what isn't
- [ ] Identify crashes and/ or raw memory data
- [ ] Debug the resulting binary
- [ ] Understand precisely why the crash happened
  - [ ] 1. What data of the memory can be manipulated based on the input data that crashes?
  - [ ] 2. Use Bruijin sequence to find offset to memory addresses
  - [ ] 3. What data structure can we exploit (stack, heap)
  - [ ] 4. What data/ fixed addresses can we pivote (global offset table, fork respawning, etc)
  - [ ] 5. Can we apply advanced exploitation techniques (i.e.: Blind ROP, ROP, Leakless)
 
