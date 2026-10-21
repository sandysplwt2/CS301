JAR_NAME = ttsDemo.jar
MAIN_CLASS = Main
CLASSPATH = .:/usr/share/java/freetts.jar

SRC = Main.java Speaker.java
CLS = Main.class Speaker.class

build: $(JAR_NAME)

$(JAR_NAME): $(CLS)
	jar cfe $(JAR_NAME) $(MAIN_CLASS) $(CLS)

Main.class: Main.java
	javac -cp "$(CLASSPATH)" Main.java

Speaker.class: Speaker.java
	javac -cp "$(CLASSPATH)" Speaker.java

run: $(JAR_NAME)
	java -cp "$(JAR_NAME):/usr/share/java/*" $(MAIN_CLASS)

clean:
	rm -f *.class $(JAR_NAME)

