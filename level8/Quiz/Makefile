SRC_DIR = ./src/
OBJ_DIR = ./obj/
HEADER_DIR = ./include/

NAME = main
SRC_NAME = main.c first.c second.c third.c
SRCS = $(addprefix $(SRC_DIR),$(SRC_NAME))
OBJ_NAME = $(SRC_NAME:.c=.o)
OBJS = $(addprefix $(OBJ_DIR),$(OBJ_NAME))

CC = gcc
CFLAGS = -Wall -Wextra -Werror

.PHONY : all clean fclean re run
all : $(NAME)
clean :
	rm -f $(OBJS)
fclean : clean
	rm -f $(NAME)
re : fclean all
run : all
	./$(NAME)

$(NAME) : $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

$(OBJ_DIR)%.o : $(SRC_DIR)%.c
	mkdir -p $(OBJ_DIR)
	$(CC) $(CFLAGS) -c $< -o $@ -I$(HEADER_DIR)
