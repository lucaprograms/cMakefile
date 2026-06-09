# Makefile for single file c file named main.c
# All .PHONY declarations
.PHONY: help
.PHONY: print
.PHONY: clean
.PHONY: enabletest
.PHONY: disabletest
.PHONY: enable
.PHONY: disable
.PHONY: allenable
.PHONY: alldisable
.PHONY: enablerun
.PHONY: disablerun
.PHONY: disableversion
.PHONY: enableversion
# end
SRC := main.c
COUNTER := version.txt
application.exe: $(SRC)
	@make incversion
	@echo ""
	@echo ""
	@echo "Compiling application exe..."
	@echo ""
	@echo ""
	@gcc main.c -o application.exe
incversion:
	@mkdir -p $(dir $(COUNTER))
	@if [ ! -f "$(COUNTER)" ]; then echo 0 > "$(COUNTER)"; fi
	@old=$$(cat "$(COUNTER)"); \
	new=$$((old + 1)); \
	echo "$$new" > "$(COUNTER).tmp" && mv "$(COUNTER).tmp" "$(COUNTER)"
delversion:
	@echo ""
	@echo ""
	@echo "Deleting version file..."
	@echo ""
	@echo ""
	@rm -f $(COUNTER)
enableversion:
	@echo ""
	@echo ""
	@echo "Enabling version.."
	@echo ""
	@echo ""
	@rm -f incversion
	@rm -f delversion
disableversion:
	@echo ""
	@echo ""
	@echo "Disabling version.."
	@echo ""
	@echo ""
	@touch incversion
	@touch delversion
enable:
	@echo ""
	@echo ""
	@echo "Enabling most options..."
	@echo ""
	@echo ""
	@make enabletest
	@make allenable
	@make enablerun
	@make enableversion
enablerun:
	@echo ""
	@echo ""
	@echo "Enabling run option..."
	@echo ""
	@echo ""
	@rm -f run
disablerun:
	@echo ""
	@echo ""
	@echo "Disabling run option..."
	@echo ""
	@echo ""
	@touch run
disable:
	@echo ""
	@echo ""
	@echo "Disabling most options..."
	@echo ""
	@echo ""
	@make disabletest
	@make alldisable
	@make disablerun
	@make disableversion
alldisable:
	@echo ""
	@echo ""
	@echo "Disabling all option..."
	@echo ""
	@echo ""
	@touch all
allenable:
	@echo ""
	@echo ""
	@echo "Enabling all option..."
	@echo ""
	@echo ""
	@rm -f all
all:
	@make help
	@make print
	@make
	@make main.c
	@make run
	@make clean
test:
	@make
	@make run
	@make clean
clean:
	@echo ""
	@echo ""
	@echo "Delelting application files..."
	@echo ""
	@echo ""
	@rm -f a*
	@rm -f A*
disabletest:
	@echo ""
	@echo ""
	@echo "Disabling test option..."
	@echo ""
	@echo ""
	@touch test
enabletest:
	@echo ""
	@echo ""
	@echo "Enabling test option..."
	@echo ""
	@echo ""
	@rm -f test
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
	@echo "make disabletest: disables the test option"
	@echo "make enabletest: enables the test option"
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
