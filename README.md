To view the slides, go to https://baremetaldev.github.io/adc20/

# adc20
Hitchhiker's Guide to Embedded Audio

# Electronics

## Analogue
Our audio journey starts (and ends) in the analogue realm. Why it's important to get this part right.
## Schematics
A visual design language with many more ways to get wrong than right.
- Kicad, intro to an open source schematic and PCB design tool.
## Circuit simulation
We'll briefly touch on circuit simulations that can help check your work.
## Digital audio circuits
We've seen what the analogue front end might look like, but how do we turn analogue signals into the digital values we need to do our work? We'll look at the tools, converters and signal standards for analuge-to-digital conversion.
- ADCs, how they do their magic.
- I2S / TDM, transmitting the data.
- I2C, controlling the magic.
- Frequencies and bit-depths.
## Microcontrollers
The most complex part of our schematic, but luckily there are plenty of rules and examples to follow.
- Power and clocks.
- Hi-speed lines.
## Datasheets
We've avoided this part for as long as we can, but now we'll have to take a look at the documentation for our microcontroller. These docs seem to hate us more than we hate the docs, but reading them is just another technique to learn.

# Baremetal Programming

## Assembly
The lowest level part of our program, just to get things running. How we create the C abstract machine and get to main()?
## C/C++
A high level language, but how do we control hardware from all the way up here?
- SFRs, our memory-mapped gods.
## Compilers
The tools we need to turn our high-level language back into assembly and running on the metal.
- GCC
- Clang
## Building
A brief look at standard build automation, why it's useful and why it can be a bit of a headache at first.
- CMake, standard open source tool for build automation.
- Visual Studio Code, open-source tool for editing, building and debugging.
## Debugging
Basic methods of debugging, from flashing an LED to stepping through the code one line at a time. How do you debug a system that has no screen to print 'hello world'?
- Debug emulators, connecting our tools to the hardware.
- GDB, running our program, stepping and getting data from the hardware.
- OpenOCD, bridging the gap between our hardware tools and our software tools.
## Peripherals
It's important to know your strengths and weaknesses. Microcontrollers tend to be slower/less-powerful, but they have special hardware built in that can do the job.
- I2C, talking to our external hardware.
- I2S, the audio stream.
- DMA, moving the data from peripherals.

# Embedded Programming

## Hard Real-Time
Some folks may be familiar with 'The Audio Thread'. Our embedded system is like one giant audio thread.
- Memory allocations
- Interrupts
- C++ exceptions, RTTI and the other features we tend to switch off.

## Stack Overflow
What happens if you run out of memory?
- Hardware exceptions.
- Memory corruption.
- Undefined behaviour.

# Audio Programming

## Audio buffers
Our I2S peripheral is bringing in all this audio. How do we interact with it? What does it look like?

## DSP
We've still got some CPU power left, so why not have a brief look at digital signal processing.
- Delays
- Filters

# Output

## USB
Now we've got some audio, let's send it to the computer. There are some fundamentals that might be useful to know here.
- Descriptors
- Endpoints
- Limitations

## Audio
Or we can send our audio back out to the real world.
- DACs, digital-to-analogue conversion.
- CODECS, audio I/O devices you might find on your dev kit.

# Conclusion

Getting started with hardware can be daunting.
- Prototyping with development boards / dev kits.
- Starting with software.
- Tutorials and youtube videos.
