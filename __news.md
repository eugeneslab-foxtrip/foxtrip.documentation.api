# News requests (20)

```` json
{
    "id"            : "1",
    "cover"         : "http://127.0.0.1/album/lorem.png",
    "datetime"      : "155748321874",
    "title"         : "Lorem Ipsum is simply dummy text of the printing",
    "content"       : "Lorem Ipsum has been the industry's standard dummy text",
    "publicated"    : "false",
}
````

- **id** - indetificator of a publication
- **cover** - path to a cover picture
- **datetime** - defines date and time UTC (without offset) in seconds when it was publicated. 
- **title** - title of publication which is limited by 98 bytes
- **content** - text of the publication. There is not limitation. The text is formated with Markdown style
- **publicated** - flag which defines if the publication is publicated