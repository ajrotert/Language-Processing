
go: lex.yy.c w.tab.c
	gcc w.tab.c lex.yy.c -lfl -ly -o go 

lex.yy.c: w.l
	flex  w.l

w.tab.c: w.y
	bison -dv w.y

clean:
	rm -f lex.yy.c 
	rm -f w.output
	rm -f w.tab.h
	rm -f w.tab.c
	rm -f go 
	rm -f tom

tom: t.sharp lex.yy.c w.tab.c
	gcc w.tab.c lex.yy.c -lfl -ly -o go
	./go < t.sharp
	gcc .tom.c -lm -o tom
