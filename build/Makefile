# Makefile for single file c file named main.c
# All .PHONY declarations
.PHONY: help
.PHONY: print
.PHONY: clean
.PHONY: run
.PHONY: all
# end
application.exe:
	@echo ""
	@echo ""
	@echo "Compiling application exe..."
	@echo ""
	@echo ""
	@gcc main.c -o application.exe
all:
	make help
	make print
	make
	make main.c
	make run
	make clean
test:
	make
	make run
	make clean
clean:
	@echo ""
	@echo ""
	@echo "Delelting application files..."
	@echo ""
	@echo ""
	@rm -f a*
	@rm -f A*
help:
	@echo ""
	@echo ""
	@echo "Help"
	@echo ""
	@echo ""
	@echo "make help: Shows this help message"
	@echo "make print: Verifys if tool exists in the current folder by printing a message"
	@echo "make all: Execute all options"
	@echo "make: Compile the application"
	@echo "make application.exe: Compile the application"
	@echo "make clean: Deletes all files starting with 'a' and 'A'"
	@echo "make run: Run the executable (application)"
	@echo ""
	@echo ""
run:
	@./application.exe
print:
	@echo ""
	@echo ""
	@echo "Makefile tool does exist in dir: /"
	@echo ""
	@echo ""
