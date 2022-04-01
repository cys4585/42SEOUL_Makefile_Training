NAME := libft.a
OBJS := first.o second.o third.o
AR := ar
ARFLAGS := rcs
CC := gcc
CFLAGS := -c

$(NAME) : $(OBJS)
	$(AR) $(ARFLAGS) $@ $?

%.o : %.c
	$(CC) $(CFLAGS) $<
