
<link rel="preload" as="style" href="https://actwu.github.io/md.css" />
<link rel="stylesheet" href="https://actwu.github.io/md.css" />


<cont>
<say>You typed.</say>
<p></p>
</cont>

<cont>
<say>Url's.</say>
<urls></urls>
</cont>
<link rel='preload' as="script" href='https://iselang.github.io/num.js'>

<script src="https://iselang.github.io/num.js"> </script>

<script type="module" src="https://iselang.github.io/num.js"> </script>
<script type="module">
app('Myurl');
fav(2);

setTimeout(async () => {
await bit.init();
let userData = await bit.get("path");
let cleanData = decodeURIComponent(userData).replace(/^\/+/, '');
pick('p').set = cleanData;

await bit.init();

let dbData = await net.get('https://myurl.github.io/db');
const listItem = pick("urls");

let urlMap = Object.fromEntries(
dbData
.trim()
.split('\n')
.map(line => line.trim())
.filter(line => line.includes('='))
.map(line => {
let [key, value] = line.split('=');
return [key.trim(), value.trim()];
})
);

Object.entries(urlMap).forEach(([key, value]) => {
let link = make("tap");
let fgu = make("say");
fgu.set=key;
link.append(fgu);
link.at = "bol2"
link.addEventListener("mousedown", (event) => {
event.preventDefault(); 
path.go(value); 
});

listItem.append(link);
});

AutoUI();

}, 50);
console.clear();

</script>
