all: compile run

.PHONY: compile run clean ast_file

compile:
	if [ ! -d "./class" ]; then mkdir class; fi
	javac -d class lox/*.java

run:
	java -cp class lox/Lox

clean:
	rm -rf class/*

ast_file:
	javac tool/GenerateAst.java
	java tool/GenerateAst lox
	rm tool/GenerateAst.class
