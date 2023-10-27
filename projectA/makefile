OBJS = lib/other1.o lib/other2.o
LIB_NAME = libcal.a
LIB_PATH = lib/$(LIB_NAME)
EXECUTABLE = main
all: $(EXECUTABLE)
lib/%.o: src/%.c
	$(CC) -c $< -o $@
$(LIB_PATH): $(OBJS)
	ar rcs $(LIB_PATH) $(OBJS)
$(EXECUTABLE): $(LIB_PATH) src/main.c
	$(CC) src/main.c -Llib -lcal -o $(EXECUTABLE)
clean:
	rm -f $(OBJS) $(LIB_PATH) $(EXECUTABLE)
