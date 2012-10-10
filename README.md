A backbone.js view that renders collections as lists or table elements and handles selection (single or multiple) and sorting of models in the collection.

Dependencies: backbone.js, jQuery, jQueryUI (for sorting)

The actual rendering of individual models in the collection is taken care of by a model view class that is injected into the collection view. The collection view keeps track of the selected model(s) and fires events when the selection is changed. It also adds the "selected" class to the "li" or "tr" dom elements that represent the selected models so you can easily add highlighting, for example, to selected elements via CSS. It supports single and multiple selection through meta-key clicks and shift clicks, just like you would expect from a SELECT box. Selected elements are dealt with intuitively after events like adding or deleting elements. For example, if the selected model is removed from the collection (or deleted), the model that immediately follow the removed model will be automatically selected (automatically skipping hidden "li" or "tr" elements, in case the list is being filtered). Sorting the collection via dragging and dropping is also supported, and appropriate events are fired so you can persist changes to the order of the models in the collection.