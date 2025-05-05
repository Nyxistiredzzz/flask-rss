# Projecte RSS Flask - Arnau Barceló González

Aquest projecte és una aplicació Flask que permet visualitzar notícies de La Vanguardia a partir de fitxers RSS.

## Requisits previs

Abans de començar, assegura't de tenir instal·lat Python 3\. També necessitaràs les llibreries següents:

- [feedparser](https://pythonhosted.org/feedparser/)
- [Flask](https://flask.palletsprojects.com/)

## Instruccions per desplegar l'aplicatiu

### 1\. Crear un entorn virtual

Un entorn virtual permet aïllar les dependències del projecte. Pots crear-lo amb la comanda següent:

```powershell
python -m venv .venv
```

### 2\. Activar l'entorn virtual

Per activar l'entorn virtual, executa:

```powershell
.venv\Scripts\activate
```

### 3\. Instal·lar les dependències

Un cop activat l'entorn virtual, instal·la les llibreries necessàries:

```powershell
pip install feedparser flask
```

### 4\. Iniciar l'aplicació

Per iniciar l'aplicació Flask, executa:

```powershell
flask run
```

L'aplicació estarà disponible a <http://127.0.0.1:5000>.

### 5\. Desactivar l'entorn virtual

Quan hagis acabat, pots utilitzar CTRL+C per sortir i després pots desactivar l'entorn virtual amb:

```powershell
deactivate
```

## Canviar entre mode remot i mode local

L'aplicació pot funcionar en dos modes:

- **Mode remot**: Descarrega l'XML directament de la web de La Vanguardia.
- **Mode local**: Utilitza un fitxer XML descarregat prèviament.

Per canviar entre aquests modes, edita la funció `get_rss_lavanguardia` al fitxer `app.py`:

- **Mode remot**: Descomenta la línia següent i comenta la línia del mode local:

  ```python
  xml = f"https://www.lavanguardia.com/rss/{seccio}.xml"
  ```

- **Mode local**: Comenta la línia del mode remot i descomenta la següent:

  ```python
  xml = f"./rss/lavanguardia/{seccio}.xml"
  ```

## Recursos addicionals

- [Què són els entorns virtuals?](https://realpython.com/python-virtual-environments-a-primer/)
