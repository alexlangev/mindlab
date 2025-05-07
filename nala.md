# Nala (apt frontend)

## Nala install / upgrade 

```sh
# upgrade installed packages?
sudo nala update
sudo nala upgrade

# delete 
sudo nala remove <NAME>
```

## Nala history (undo redo)
```sh
# list history on commands
sudo nala history

# undo a command
sudo nala history undo <ID>

# redo a command
sudo nala history redo <ID>
```


## Install Nala

```sh
sudo apt install nala
```

## Autoselect fastest mirrors

```sh
sudo nala fetch
```
