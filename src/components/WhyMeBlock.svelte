<script>
    export let img_src = '/project/thumbnail.png'
    export let img_alt = 'Error 418 : Server Refuse to Brew'
    export let title_string = 'title_string={?}'
    export let extra_string = "extra_string={?}";
</script>

<div>
    <img src={img_src} class="px-5 mb-3" alt={img_alt}>
    <h3 class="text-2xl font-semibold text-center mb-2">{title_string}</h3>
    <p class="text-lg text-center">{extra_string}</p>
</div>