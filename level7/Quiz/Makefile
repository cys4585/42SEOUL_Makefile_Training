NAME := main
SRCS := main.c
OBJS := $(SRCS:.c=.o)

LIBFT := libft.a
LIB_SRCS := first.c second.c third.c
LIB_OBJS := $(LIB_SRCS:.c=.o)

AR := ar
ARFLAGS := rcs
CC := gcc
CFLAGS := -Wall -Wextra -Werror

.PHONY : all clean fclean
all : $(NAME)
clean :
	rm -f *.o
fclean :
	rm -f $(LIBFT) $(NAME)
re : clean fclean all

$(NAME) : $(LIBFT) $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

$(LIBFT) : $(LIB_OBJS)
	$(AR) $(ARFLAGS) $@ $?

%.o : %.c
	$(CC) $(CFLAGS) -c $<
