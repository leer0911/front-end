# FrontEnd

<diff :height=600 :original="original" :modified="modified">
</diff>
<flow :code="code"></flow>

<script>
const original =
`
  var a = 1;
  var b = 2;

`
const modified =
`
 const a = 1;
 const b = 2;
`
const code =
`
function indexSearch(list, element) {
    let currentIndex,
        currentElement,
        minIndex = 0,
        maxIndex = list.length - 1;

    while (minIndex <= maxIndex) {
        currentIndex = Math.floor(minIndex + maxIndex) / 2;
        currentElement = list[currentIndex];

        if (currentElement === element) {
            return currentIndex;
        }

        if (currentElement < element) {
            minIndex = currentIndex + 1;
        }

        if (currentElement > element) {
            maxIndex = currentIndex - 1;
        }
    }

    return -1;
}
`
module.exports = {
    data(){
        return{
            original,
            modified,
            code
        }
    }
}
</script>
