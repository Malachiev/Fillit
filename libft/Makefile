# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: gconroy <gconroy@student.42.fr>            +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/11/30 21:36:03 by gconroy           #+#    #+#              #
#    Updated: 2019/04/01 13:37:01 by gconroy          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a

OBJ = $(patsubst %.c, %.o, $(wildcard *.c))

FLAG = -Wall -Wextra -Werror

HEADER = includes/libft.h

all: $(NAME)

$(NAME): $(OBJ)
	ar -rc $(NAME) $(OBJ)
	ranlib $(NAME)
	
%.o: %.c $(HEADER)
	gcc $(FLAG) -c $< -o $@ -I./includes
	
ex: $(NAME)
	gcc $(FLAG) main.c $(NAME)

clean:
	/bin/rm -f $(OBJ)
	
fclean: clean
	/bin/rm -f $(NAME)
	
re: fclean all
