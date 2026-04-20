# dotfiles

Configuración personal de terminal para macOS — optimizada para baja fatiga ocular y productividad.

## Qué incluye

- **Ghostty** — terminal moderna y rápida (Apple Silicon nativo)
- **Gruvbox Dark** — tema de colores cálidos, diseñado para sesiones largas
- **JetBrains Mono 15px** — fuente diseñada para código, con ligaduras
- **zsh-syntax-highlighting** — colorea comandos en tiempo real mientras escribes
- **zsh-autosuggestions** — sugiere comandos basándose en tu historial
- **Starship** — prompt minimalista con información útil

## Requisitos previos

macOS con Apple Silicon (M1/M2/M3/M4) y Homebrew instalado.

Si no tienes Homebrew:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Instalación en un Mac nuevo

### 1. Instalar Ghostty

```bash
brew install --cask ghostty
```

### 2. Instalar la fuente

```bash
brew install --cask font-jetbrains-mono
```

### 3. Instalar los plugins de zsh

```bash
brew install zsh-syntax-highlighting zsh-autosuggestions
```

### 4. Instalar Starship

```bash
brew install starship
```

### 5. Clonar este repositorio

```bash
git clone https://github.com/Juanmaria-rr/dotfiles.git ~/.dotfiles
```

### 6. Copiar los ficheros de configuración

```bash
cp ~/.dotfiles/.zshrc ~/.zshrc
mkdir -p ~/.config/ghostty
cp ~/.dotfiles/ghostty-config ~/.config/ghostty/config
mkdir -p ~/.config
cp ~/.dotfiles/starship.toml ~/.config/starship.toml
```

### 7. Recargar zsh

```bash
source ~/.zshrc
```

### 8. Reiniciar Ghostty

Cierra y vuelve a abrir Ghostty. Debería arrancar con Gruvbox Dark, JetBrains Mono y el prompt de Starship.

## Atajos de zsh útiles

| Atajo | Acción |
|-------|--------|
| `Ctrl+A` | Ir al inicio de la línea |
| `Ctrl+E` | Ir al final de la línea |
| `Ctrl+W` | Borrar la palabra anterior |
| `Ctrl+U` | Borrar toda la línea |
| `Ctrl+L` | Limpiar la pantalla |
| `Ctrl+R` | Buscar en el historial |
| `Ctrl+C` | Cancelar el comando actual |
| `Ctrl+Z` | Pausar el proceso actual |
| `!!` | Repetir el último comando (útil: `sudo !!`) |
| `!$` | Reutilizar el último argumento |

## Mantener actualizado

Cada vez que cambies algo en tu configuración:

```bash
cd ~/.dotfiles
cp ~/.zshrc .
cp ~/.config/starship.toml .
cp ~/.config/ghostty/config ghostty-config
git add .
git commit -m "descripción del cambio"
git push
```
