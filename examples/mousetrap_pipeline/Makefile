comp:
	iverilog -I../../tb_lib  -I$(OVL_TOP) -I$(OVL_TOP) -DNO_RAM_INIT -DDEBUG -DOVL_ASSERT_ON -DOVL_VERILOG -o tb  -c vlist_tb.txt

run:
	vvp tb +program_memory=test.vmem

wave:
	gtkwave tb.vcd


help:
	@echo "Targets:"
	@echo "         comp : Compile the design with icarus Verilog (using files listed in vlist_tb.txt)"
	@echo "         run : Run the simulation using file test.vmem,, generating a vcd file"
	@echo "         wave  : View the vcd file using gtkwave vcd viewer"




# For flymake on-the-fly code checking
check-syntax:
	iverilog -t null -I../../tb_lib -o tb  -c vlist_tb.txt
