<template>
    <my-page title="首页">
        <form id="previewform" action="">
            <h1>GitHub &amp; BitBucket HTML Preview</h1>
            <p>Enter URL of the HTML file to preview: <input type="url" id="file" value="" placeholder="e.g. https://github.com/user/repo/blob/master/index.html" size="60" autofocus> <input type="submit" value="&raquo;"></p>
            <p>or prepend to the URL: <strong>http://htmlpreview.github.io/?</strong>https://github.com/twbs/bootstrap/blob/gh-pages/2.3.2/index.html</p>
            <p>or use this bookmarklet while browsing GitHub or BitBucket: <a href="javascript:void('http://htmlpreview.github.io/'==window.location?alert('Drag me to your bookmarks bar!'):window.location='http://htmlpreview.github.io/?'+window.location)"><strong>HTMLPreview</strong></a></p>
            <p id="footer">Developed by <a href="https://github.com/niutech">niu tech</a> | Contribute on <a href="https://github.com/htmlpreview/htmlpreview.github.com">GitHub</a></p>
        </form>
    </my-page>
</template>

<script>
    const HTMLPreview = window.HTMLPreview

    export default {
        data () {
            return {
                page: {
                    menu: [
                        {
                            type: 'icon',
                            icon: 'help',
                            to: '/help'
                        }
                    ]
                }
            }
        },
        mounted() {
            HTMLPreview.previewform = document.getElementById('previewform')
            HTMLPreview.init()
        }
    }
</script>

<style scoped>
body {
    font: 12px 'Helvetica Neue', Helvetica, Arial, freesans, clean, sans-serif;
    color: #333;
}
h1 {
    font-size: 20px;
}
a {
    color: #666;
}
form {
    padding: 20px; 
    text-align: center;
}
strong {
    color: #333;
    background-color: #FAFFA6;
    padding: 0.1em;
}
#footer {
    margin: 20px 0;
    font-size: 10px;
    color: #666;
}
</style>
