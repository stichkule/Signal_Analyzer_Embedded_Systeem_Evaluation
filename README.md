# Signal_Analyzer_Embedded_System_Evaluation
This project is intended to serve as a high level design and analysis methodology, for the design evaluation of a Signal Analyzer. Based on the design and performance requirements desired by the client, simulations and tests were carried out using an evaluation board with the aid of external hardware and software components. Using these test results, which are listed as project deliverables, the suitability of the STM32F401RE microcontroller for the Signal Analyzer application was evaluated, along with providing recommendations pertaining to full system design and performance.

Pursuant to the Request for Services (RFS), the
suitability of the STM32F401RE microcontroller (MCU) was evaluated for the design of
their Signal Analyzer product. The NUCLEO-F401RE evaluation board was used in
conjunction with analog and digital peripherals to test hardware performance aspects of
this MCU. Software performance was qualitatively and quantitatively tested based upon
the ability of the MCU to execute interrupt-driven, concurrent, and processing intensive
tasks. The most critical test results and findings pertaining to the design evaluation of the
STM32F401RE MCU for the Signal Analyzer application are listed below.

• The MCU was able to be successfully interfaced with a serial terminal, which can
serve as a natural, and easy-to-use debugging tool. Further, the STM32F401RE MCU
was found to run at ca. 98 DMIPS, which agrees with the specified requirements for
the Signal Analyzer application.

• Synthesis of audio waves (20 Hz — 20 kHz) was accomplished using the MCU, such
that the frequency and amplitude could be adjusted by the use of potentiometers.
Further, SPDT button switches could be used to control the blinking of LEDs based
on wave parameters. These are essential functionalities for a signal generator/
harmonic analyzer, and the STM32F401RE MCU facilitated their implementation
with ease.

• Real time performance was qualitatively measured by observing the ability of the
STM32F401RE MCU to respond to interrupt-driven events. RTOS functionality such
as threads were implemented and concurrently executed in a cyclic executive to service
peripheral interrupts. The MCU was found to execute these tasks without any visible
latency or jitter issues.

• Floating point samples of an audio wave signal with a predetermined frequency of
1004 Hz were provided externally to the STM32F401RE MCU. An autocorrelation
based peak-detection algorithm was implemented and executed on the MCU, which
was able to estimate the input audio frequency with an accuracy of 0.4%.
