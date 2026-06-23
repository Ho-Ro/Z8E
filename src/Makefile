# TAGET is either z8e (Z80) or 18e (HD64180)
TARGET = z8e

# CFG is $(TARGET)1.inc (one terminal) or $(TARGET)2.inc (separate debug terminal)
CFG = $(TARGET)1.inc

SRC = z8e.z80

COM = $(TARGET).com
LST = $(TARGET).lst


all: $(COM)


$(COM): $(SRC) $(INC) Makefile
	@rm -f config.inc
	@ln -s $(CFG) config.inc
	zx80asm $(TARGET)/as


.PHONY: clean
clean:
	rm -f $(COM) $(LST)
