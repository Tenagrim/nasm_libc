.PHONY: all clean fclean re
NAME=libasm.a
HEADER=libasm.h
SRC=ft_strlen.s \
	ft_strcmp.s \
	ft_strcpy.s \
	ft_strdup.s \
	ft_write.s \
	ft_read.s
OBJ=$(SRC:.s=.o)

all: $(NAME)

$(NAME): $(OBJ)
	ar -rc $(NAME) $(OBJ)
	ranlib $(NAME)

%.o: %.s
	nasm -f macho64 $<

clean:
	rm -f $(OBJ)

fclean: clean
	rm -f $(NAME)

re: fclean all
