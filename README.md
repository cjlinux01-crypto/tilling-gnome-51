# 🪟 SolusTiling (Pop Shell para GNOME 51)

**O que é o SolusTiling?**  
O **SolusTiling** é uma versão adaptada e corrigida da famosa extensão **Pop Shell** (da System76) feita para rodar perfeitamente no **GNOME 51**. 

Com ele, o seu sistema ganha **auto-tiling automático** (as janelas se organizam e dividem a tela sozinhas assim que são abertas), gerenciamento completo por atalhos de teclado e o menu pesquisável de aplicativos e janelas (*Launcher*), tudo corrigido para não apresentar os erros de incompatibilidade das versões recentes do GNOME.

---

## 🚀 Passo a Passo de Instalação

### 1. Baixar o arquivo
Clique no arquivo **`solustilling@mendes.local.shell-extension.zip`** disponível acima neste repositório e clique no botão **Download** (ícone de seta para baixo no canto direito) para salvá-lo na sua pasta de **Downloads**.

### 2. Instalar pelo Terminal
Abra o seu terminal, entre na pasta onde o arquivo foi baixado e instale a extensão rodando o comando único abaixo:

```bash
cd ~/Downloads && gnome-extensions install --force solustilling@mendes.local.shell-extension.zip && gnome-extensions enable solustilling@mendes.local
```
*(Nota: Se o seu sistema estiver em português e a pasta se chamar `Transferências`, troque `~/Downloads` por `"$(xdg-user-dir DOWNLOAD)"`).*

### 3. Recarregar a sessão (Importante para Wayland)
Se você usa sessão **Wayland** (padrão no GNOME 51), o sistema só carrega extensões recém-instaladas após reiniciar a sessão do usuário:

1. Faça **Logout (Encerrar Sessão)** no menu do sistema e faça **Login** novamente (ou rode `gnome-session-quit --logout --no-prompt` no terminal).
2. Ao voltar para a área de trabalho, execute o comando de ativação para confirmar que ela está ligada:

```bash
gnome-extensions enable solustilling@mendes.local
```

Pronto! O ícone do **SolusTiling** já vai aparecer na sua barra superior do GNOME.

---

## ⌨️ Atalhos Globais de Teclado (Opcional)

Se os atalhos de teclado (como `Super + Y` para ligar/desligar o auto-tiling ou `Super + /` para abrir o Launcher) não funcionarem de primeira, rode este comando para registrar os atalhos no sistema:

```bash
sudo cp ~/.local/share/gnome-shell/extensions/solustilling@mendes.local/schemas/*.xml /usr/share/glib-2.0/schemas/ && sudo glib-compile-schemas /usr/share/glib-2.0/schemas/
```
