SRC_DIR = ./src/
OBJ_DIR = ./obj/
LIB_DIR = ./lib/
HEADER_DIR = ./include/

NAME = main
SRC_NAME = main.c fourth.c
SRCS = $(addprefix $(SRC_DIR),$(SRC_NAME))
OBJ_NAME = $(SRC_NAME:.c=.o)
OBJS = $(addprefix $(OBJ_DIR),$(OBJ_NAME))

LIB_NAME = ft
LIB = $(LIB_DIR)lib$(LIB_NAME).a

CC = gcc
CFLAGS = -Wall -Wextra -Werror
INCLUDE = -I$(LIB_DIR) -I$(HEADER_DIR)

.PHONY : all clean fclean re run
all : $(NAME)
clean :
	rm -f $(OBJS)
	make -C $(LIB_DIR) clean
fclean : clean
	rm -f $(NAME)
	make -C $(LIB_DIR) fclean
re : fclean all
run : all
	./$(NAME)

$(NAME) : $(LIB) $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

$(LIB) :
	make -C $(LIB_DIR) all

$(OBJ_DIR)%.o : $(SRC_DIR)%.c
	mkdir -p $(OBJ_DIR)
	$(CC) $(CFLAGS) $(INCLUDE) -c $< -o $@
