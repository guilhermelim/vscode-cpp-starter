# vscode-cpp-starter

Este projeto fornece um template básico para iniciar um projeto C++ com CMake e MSYS2 no Visual Studio Code. A configuração inclui suporte para C++23 e uma estrutura de projeto recomendada para desenvolvimento com o VS Code.

## Estrutura do Projeto

```

vscode-cpp-starter/
├── CMakeLists.txt
├── include/
│   └── (arquivos de cabeçalho, se houver)
├── src/
│   ├── CMakeLists.txt
│   └── main.cpp
└── build/ (gerado pelo CMake)

```

## Requisitos

- **MSYS2**: Para Windows, você pode baixar a versão mais recente do [MSYS2](https://github.com/msys2/msys2-installer/releases).
- **Visual Studio Code**: IDE recomendada para editar e depurar o código.
- **CMake**: Ferramenta de construção para gerenciar o processo de construção do projeto.
- **GCC**: Compilador C++ incluído com MSYS2.

## Configuração do Ambiente

1. **Instale o MSYS2**:
   - Siga as instruções fornecidas na [página de instalação do MSYS2](https://github.com/msys2/msys2-installer/releases).

2. **Instale o GCC e o CMake**:
   - Abra o terminal MSYS2 e execute:

     ```sh
     pacman -Syu
     pacman -S mingw-w64-x86_64-cmake mingw-w64-x86_64-gcc mingw-w64-x86_64-gdb
     ```

3. **Adicione o MSYS2 ao PATH**:
   - Adicione o diretório do MSYS2 ao PATH do Windows. Isso pode ser feito em `Configurações do Sistema > Avançado > Variáveis de Ambiente`:

     ```
     C:\msys64\mingw64\bin
     ```

## Compilação e Execução

1. **Configure o Projeto**:
   - Abra o Visual Studio Code e carregue o projeto.
   - Na paleta de comandos (`Ctrl+Shift+P`), selecione `CMake: Configure`.

2. **Compile o Projeto**:
   - Na paleta de comandos (`Ctrl+Shift+P`), selecione `CMake: Build` ou pressione `F7`.

3. **Execute o Projeto**:
   - Vá para o painel de depuração (`Ctrl+Shift+D`), selecione a configuração `Debug (g++)` e clique no botão verde de play ou pressione `F5`.

## Estrutura dos Arquivos

- **`CMakeLists.txt`**: Arquivo principal de configuração do CMake.
- **`src/main.cpp`**: Código-fonte principal do projeto.
- **`include/`**: Diretório para arquivos de cabeçalho.
- **`build/`**: Diretório gerado pelo CMake para arquivos de construção.

## Nota

Certifique-se de que a versão do CMake utilizada é compatível com C++23. Se necessário, ajuste o arquivo `CMakeLists.txt` para refletir alterações no ambiente ou nos requisitos do projeto.
