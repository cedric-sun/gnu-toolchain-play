default:
	@echo "Doing nothing. Available targets: share wrong right0 right1 clean"

share:
	gcc -o lib.so -shared -fPIC lib.c

wrong: share
	gcc -o main.elf main.c lib.so

right0: share
	gcc -o main.elf main.c ./lib.so

right1: share
	gcc -o main.elf main.c lib.so -Xlinker -rpath ./

clean:
	rm -f lib.so main.elf
