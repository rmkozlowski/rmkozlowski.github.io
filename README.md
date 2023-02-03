# rmkozlowski.github.io
<html>
<SCRIPT>
    var pos = 0;
    const pacArray = [
        ['PacMan1.png', 'PacMan2.png'],
        ['PacMan3.png', 'PacMan4.png']
    ];

    var direction = 0;
    var focus = 0;

    function Run() {
        let img = document.getElementById("PacMan");
        let imgWidth = img.width
        focus = (focus + 1) % 2;
        direction = checkPageBounds(direction, imgWidth);
        img.src = pacArray[direction][focus];
        if (direction) {
            pos -= 20;
            img.style.left = pos + "px";
        } else {
            pos += 20;
            img.style.left = pos + 'px';
        }
        // Use setTimeout to call Run every 200 millesecs
    }
    setTimeout(Run, 300);

    function checkPageBounds(direction, imgWidth) {
        //
        // Complete this to reverse direction on hitting page bounds
        if (direction == 0 && pos + imgWidth > pageWidth) direction = 1;
  if (direction == 1 && pos < 0) direction = 0;
  return direction;        

    }
</SCRIPT>

<body>
    <img id="PacMan" src="PacMan1.png" width='200' onclick="Run()" style="position:absolute"> </img>
</body>

</html>

![PacMan1](https://user-images.githubusercontent.com/120128966/216724026-56095606-fcd2-4f5e-ab5b-598a6a6a8aba.png)
![PacMan2](https://user-images.githubusercontent.com/120128966/216724042-70086d83-d5d0-4acb-b494-7a1c59c5c9a9.png)
![PacMan3](https://user-images.githubusercontent.com/120128966/216724053-e892d873-a1b9-477f-aa21-4808d8941b2f.png)
![PacMan4](https://user-images.githubusercontent.com/120128966/216724060-9229b059-b046-4652-8bec-984012e42c3a.png)
