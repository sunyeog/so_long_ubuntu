NAME = libft.a
SRC = ft_itoa.c ft_memchr.c ft_strchr.c ft_strrchr.c ft_memcmp.c\
	ft_strdup.c ft_strtrim.c ft_atoi.c ft_memcpy.c ft_striteri.c\
	ft_substr.c ft_bzero.c ft_memmove.c ft_strjoin.c ft_tolower.c\
	ft_calloc.c ft_memset.c ft_strlcat.c ft_toupper.c ft_isalnum.c\
	ft_putchar_fd.c  ft_strlcpy.c ft_isalpha.c  ft_putendl_fd.c ft_strlen.c\
	ft_isascii.c ft_putnbr_fd.c ft_strmapi.c ft_isdigit.c ft_putstr_fd.c\
	ft_strncmp.c ft_isprint.c ft_split.c ft_strnstr.c ft_printf.c\
	type.c type2.c type3.c
OBJ = $(SRC:.c=.o)
BSRC = ft_lstadd_back_bonus.c ft_lstclear_bonus.c ft_lstiter_bonus.c\
	   ft_lstmap_bonus.c ft_lstsize_bonus.c ft_lstadd_front_bonus.c\
	   ft_lstdelone_bonus.c ft_lstlast_bonus.c ft_lstnew_bonus.c
BOBJ = $(BSRC:.c=.o)	
HEADER = ./libft
CFLAG = -Wall -Wextra -Werror
ifdef BONUS_ON
	SRCS = $(SRC) $(BSRC)
	OBJECTS = $(OBJ) $(BOBJ)
else
	SRCS = $(SRC)
	OBJECTS = $(OBJ)
endif
all : $(NAME)
$(NAME) : $(OBJECTS)
	cc $(CFLAG) -I$(HEADER) -c $(SRCS)
	ar -rcs $(NAME) $(OBJECTS)
clean :
	/bin/rm -f $(OBJ) $(BOBJ)
fclean : clean
	/bin/rm -f $(NAME)
re : fclean all
bonus :	
	make BONUS_ON=1 all
