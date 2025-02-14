---
title: Node.parentNode
slug: Web/API/Node/parentNode
translation_of: Web/API/Node/parentNode
---
{{APIRef("DOM")}}

La propiedad de sólo lectura **`node.parentNode`** devuelve el padre del nodo especificado en el árbol.

## Sintaxis

```
parentNode = node.parentNode
```

parentNode es el padre del nodo actual. El padre de un elemento es un nodo del tipo `Element`, un nodo `Document`, o un nodo `DocumentFragment.`

## Ejemplo

```js
if (node.parentNode) {
  // Borra un nodo del árbol a no ser que
  // esté ya en el árbol
  node.parentNode.removeChild(node);
}
```

## Notas

Los nodos del tipo `Document` y `DocumentFragment` nunca van a tener un elemento padre, `parentNode` devolverá siempre `null`.

También devuelve `null` si el nodo acaba de ser creado y no está atado/incorporado al árbol.

## Compatiblidad de navegador

{{Compat("api.Node.parentNode")}}

## Especificación

- [DOM Level 2 Core: Node.parentNode](http://www.w3.org/TR/DOM-Level-2-Core/core.html#ID-1060184317)
- [DOM Level 3 Core: Node.parentNode](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-1060184317)

## Ver también

- {{Domxref("Node.firstChild")}}
- {{Domxref("Node.lastChild")}}
- {{Domxref("Node.childNodes")}}
- {{Domxref("Node.nextSibling")}}
- {{Domxref("Node.parentElement")}}
- {{Domxref("Node.previousSibling")}}
- {{Domxref("Node.removeChild")}}
