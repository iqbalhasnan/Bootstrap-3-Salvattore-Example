# Bootstrap 3 + Salvattore Example
================================

Salvattore is a jQuery Masonry alternative with CSS-driven configuration.

Steps

1. Inside a container, create a div id post and add 'data-columns' next to it <div id="posts" data-columns>

2. Configure how the images should be displayed using the CSS media queries

becomes
/* Salvattore Base Styles */
.column {
    float: left;
}
.size-1of4 {
    width: 25%;
}
.size-1of3 {
    width: 33.333%;
}
.size-1of2 {
    width: 50%;
}

/* Configurate salvattore with media queries */
@media screen and (max-width: 450px) {
    #posts[data-columns]::before {
        content: '2 .column.size-1of2';
    }
}

@media screen and (min-width: 451px) and (max-width: 850px) {
    #posts[data-columns]::before {
        content: '3 .column.size-1of3';
    }
}

@media screen and (min-width: 851px) {
    #posts[data-columns]::before {
        content: '4 .column.size-1of4';
    }
}
    
