.PHONY: all
all: rc-winch-controller-uart rc-winch-controller-servo


#############################################################################
.PHONY: rc-winch-controller-uart
rc-winch-controller-uart: rc-winch-controller-uart.hex

rc-winch-controller-uart.hex: winch-controller.o uart-input.o
	sdcc --use-non-free -mpic14 -p12f1840 -o $@ $^


#############################################################################
.PHONY: rc-winch-controller-servo
rc-winch-controller-servo: rc-winch-controller-servo.hex

rc-winch-controller-servo.hex: winch-controller.o servo-input.o
	sdcc --use-non-free -mpic14 -p12f1840 -o $@ $^


#############################################################################
.c.o:
	sdcc --use-non-free -mpic14 -p12f1840 -c $<


clean :
	$(RM) *.hex
	$(RM) *.lst
	$(RM) *.map
	$(RM) *.cod
	$(RM) *.o
	$(RM) *.asm
	
