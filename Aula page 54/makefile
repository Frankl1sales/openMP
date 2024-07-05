# Nome do executável
EXEC = testefirst

# Arquivos fonte
SRC = first.c

# Compilador e flags
CC = gcc
CFLAGS = -fopenmp

# Regras
.PHONY: all clean run help install

all: $(EXEC)

$(EXEC): $(SRC)
	$(CC) $(CFLAGS) $< -o $@ -lpthread

clean:
	rm -f $(EXEC) *.o

run: $(EXEC)
	./$(EXEC)

help:
	@echo "Makefile para compilar e executar um programa C com OpenMP"
	@echo
	@echo "Comandos disponíveis:"
	@echo "  make         - Compila o programa"
	@echo "  make clean   - Remove o executável e arquivos objeto"
	@echo "  make run     - Executa o programa"
	@echo "  make help    - Mostra esta mensagem de ajuda"
	@echo "  make install - Instala as dependências necessárias (GCC e OpenMP)"

install:
	@echo "Instalando dependências..."
	# Comandos para instalação das dependências (exemplo para sistemas baseados em Debian)
	sudo apt-get update
	sudo apt-get install -y gcc libomp-dev
	@echo "Dependências instaladas com sucesso."

