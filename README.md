# Labeling

##  Linux

1. Posizionarsi nella cartella desiderata e clonare il programma Yolo_Mark.
```
git clone https://github.com/AlexeyAB/Yolo_mark
```

2. Compilare il programma.
```
cmake .
make
```

3. Rendere il programma eseguibile e lanciarlo per verificare il corretto funzionamento.
```
chmod u+x program_name
./linux_mark.sh
```

4. Andare in `.../Yolo_Mark/x64/Release/data` e modificare `obj.data` con:
```
classes= 3
train  = data/train.txt
valid  = data/train.txt
names = data/obj.names
backup = backup/
```
ed `obj.names` con

```
blue-cone
yellow-cone
orange-cone
```
5. Cancellare le immagini già presenti in `.../Yolo_Mark/x64/Release/data/img` ed inserire [le proprie](https://photos.google.com/share/AF1QipONRHwgfi2OoVvSWzePQ2oaVHdzKbzj_URpJxN6DmiDjSvkzSOFgQg2GXja1S-Wlg?key=Y1lOZ2N2c2x5YnNuY1FiVVhBS2JJUkRJWFd4RDVB).
   
6. Riaprire il programma e per ogni immagine tracciare dei box intorno ai coni il più precisi possibile con la label corrispondente. Si possono cambiare label con i tasti 0, 1, e 2 oppure con lo slider dell'interfaccia. Una volta finita un'immagine passare alla prossima. Quando si vuole uscire basta premere ESC e tutti le label saranno salvate.

### Instruction manual

#### Mouse control

Button | Description | 
--- | --- |
Left | Draw box
Right | Move box

#### Keyboard Shortcuts

Shortcut | Description | 
--- | --- |
<kbd>→</kbd> | Next image |
<kbd>←</kbd> | Previous image |
<kbd>r</kbd> | Delete selected box (mouse hovered) |
<kbd>c</kbd> | Clear all marks on the current image |
<kbd>p</kbd> | Copy previous mark |
<kbd>o</kbd> | Track objects |
<kbd>ESC</kbd> | Close application |
<kbd>n</kbd> | One object per image |
<kbd>0-9</kbd> | Object id |
<kbd>m</kbd> | Show coords |
<kbd>w</kbd> | Line width |
<kbd>k</kbd> | Hide object name |
<kbd>h</kbd> | Help |

## Windows

1. Scaricare [Yolo_Label](https://drive.google.com/open?id=1MJyMcqRKhiNPzJkRPQ2CmGePK9XddBNP) e le [immagini raw](https://photos.google.com/share/AF1QipONRHwgfi2OoVvSWzePQ2oaVHdzKbzj_URpJxN6DmiDjSvkzSOFgQg2GXja1S-Wlg?key=Y1lOZ2N2c2x5YnNuY1FiVVhBS2JJUkRJWFd4RDVB).

2. Creare un file .txt nella stessa directory dove si trova la cartella con le immagini, con all'interno i nomi delle labels:
```
blue-cone
yellow-cone
orange-cone
```

3. Eseguire YoloLabel.exe, cliccare su open files e selezionare la cartella in cui ci sono le immagini e il file testo con le labels.

4. Per ogni immagine tracciare dei box intorno ai coni il più precisi possibile con la label corrispondente.


## SHORTCUTS

| Key | Action |
|---|:---:|
| `A` | Save and Prev Image  |
| `D,  Space` | Save and Next Image |
| `S` | Next Label <br> ![ezgif-5-f7ee77cd24c3](https://user-images.githubusercontent.com/35001605/47703190-d3049a00-dc62-11e8-846f-5bd91e98bdbc.gif)  |
| `W` | Prev Label <br> ![ezgif-5-ee915c66dad8](https://user-images.githubusercontent.com/35001605/47703191-d39d3080-dc62-11e8-800b-986ec214b80c.gif)  |
| `Ctrl + S` | Save |
| `Ctrl + C` | Delete all existing bounding boxes in the image |

| Mouse | Action |
|---|:---:|
| `Right Click` | Delete Focused Bounding Box in the image <br> ![ezgif-5-8d0fb51bec75](https://user-images.githubusercontent.com/35001605/47706913-c20d5600-dc6d-11e8-8a5c-47065f6a6416.gif) |
| `Wheel Down` | Save and Next Image  |
| `Wheel Up` | Save and Prev Image |
