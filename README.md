# My-Run-of-Execute-dynamic-circuits-
This is my run of the "Execute dynamic circuits" notebook provided by IBM Quantum Compute Documentation. I mostly kept the notebook unchanged, except I made sure to include my channel when calling QiskitIBMRuntime. The HTML file mainly serves to show that I have run a dynamic circuit on a real quantum device. 

What I learned:

How to use the MidCircuitMeasure method when creating dynamic circuits.
Qiskit Runtime limitations such as creating an if_test with 32 classical bits or less or testing only one classical bit and to not make nested conditionals.

Installation & Usage: To open this up, I used Ubuntu to create a Python environment. This was done by opening Ubuntu and placing the following commands:

python3 -m venv venv source venv/bin/activate jupyter lab --no-browser --ip=0.0.0.0 --port [insert a port number] To run this, however, you will need to create a new runtime service.

To create a service to run on quantum hardware, be sure to implement the following code with at least this much information at the beginning of your cells: QiskitRuntimeService.save_account( channel="insert appropriate channel", token='insert API key', instance="insert CRN number", overwrite=True )
