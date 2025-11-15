# Report

| Verified by | Date |
|:------------|:-----|
|`TODO`|`TODO`|

## Speculation

> In your own words, describe what the 6522 tester code does.

The tester code verifies the 6522 is wired correctly. It sets all the DDRBs to 1s, configuring them to output. It then enters an infinite loop that alternates the output pattern.

> There are some addresses dedicated to using the interface. What are they and what do they seem to do?
> _HINT_: for this part, focus on the wiring of the _address bus lines_.

$6000 to $600F range. Register Select is the lowest address bus lines. Chip Select are the higher address bus lines. Ensures address starts with $6.

> Why is creating specific, separate addresses important to achieve this function?

Crucial for Memory Mapped I/O. Since the 6502 CPU shares a single address bus for nemory and I/O devices, they're required to distinguish the VIA from other components.

> What is the value of the interface module (i.e. what does it _do_)?

It latches, buffers and manages the timing of the circuit.
