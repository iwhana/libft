# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: iwhana <iwhana@student.21-school.>         +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/10/16 19:19:48 by iwhana            #+#    #+#              #
#    Updated: 2021/11/02 19:11:46 by amalia           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a
CC = gcc
FLAG = -Wall -Wextra -Werror
SRC = ft_isalpha.c ft_isdigit.c ft_isalnum.c ft_isascii.c ft_isprint.c ft_strlen.c ft_memset.c ft_bzero.c ft_memcpy.c ft_memmove.c ft_strchr.c ft_strrchr.c ft_strlcat.c ft_strlcpy.c ft_toupper.c ft_tolower.c ft_strncmp.c ft_memcmp.c ft_memchr.c ft_strnstr.c ft_atoi.c ft_calloc.c ft_strdup.c ft_substr.c ft_strjoin.c ft_strtrim.c ft_split.c ft_itoa.c ft_strmapi.c ft_striteri.c ft_putchar_fd.c ft_putstr_fd.c ft_putendl_fd.c ft_putnbr_fd.c
OBJ = ${patsubst %.c,%.o,${SRC}}
D_FILES = ${patsubst %.c,%.d,${SRC}}
RM = /bin/rm -f

all : ${NAME}

${NAME} : ${OBJ}
	ar rcs ${NAME} $?

so:
	${CC} -nostartfiles -fPIC ${FLAG} ${SRC}
	gcc -nostartfiles -shared -o libft.so ${OBJ}

%.o : %.c
	${CC} ${FLAG} -c $< -o $@ -MD

include ${wildcard ${D_FILES}}

clean :
	${RM} ${OBJ} ${D_FILES}

fclean : clean
	${RM} ${NAME}

re : fclean all

.PHONY : all clean fclean re
