# chess-sets
6 sets of chess figures encoded as base 64 strings suited to be used as src for <img> tags, stuffed in 'chessSets' object.

### Motivation
Having developed quite a bunch of web chessboards ([ChessBoard](https://github.com/sandy98/chess-board), [Vue Chessboard](https://github.com/sandy98/vue-chessboard) and [Next Chess Board (React.js)](https://github.com/sandy98/next-chess-board) I found somewhat unpleasant to carry around the image assets, which, even when state of the art bundlers get them stuffed in the distribution bundle, have to be copied to any new project involving a chess board. So, chess-sets was born

It just consists of a single file (although in 2 versions: `chess-sets.js` - the ES6 module version - and `chess-sets.amd-cs.js` - the CS / AMD versión, also suitable to be used with no imports at all - 

The file provides a single object `chessSets`, which contains 6 keys: `alt1, default, eyes, modern, spatial, veronika`, each corresponding to a different set of figures. Each key contains 6 subkeys for the white figures and 6 for the black figures.

### Usage

```html
<img id="K-figure" />
<script src="chess-sets.amd-cs.js"></script>
<script>
    var imgK = document.getElementById('K-figure');
    imgK.src = chessSets.default.K;
</script>
```

And that's pretty much all. An example can be found inside the test directory.
