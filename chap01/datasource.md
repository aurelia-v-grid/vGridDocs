# datasource

Methods in default Datasource, see the "About" for how to create datasource


######setArray(array: Entity[]): void
* Replaces internal collection and clear internal selection/sorting and grouping

---

######push(array: Entity[]): void
* Adds to internal/displayed collection and reruns sort and grouping

---

######refresh(data?: any): void 
* Replace collection if array is passed in and rerun sort and groupings
* If no data is added it just reruns sorting and grouping

---

######select(row: number): void
* Sets row passed in as current entity

---


######query(options: FilterObject[]): void
* Queries all entities with paramas passed in

---


######orderBy(attribute: string | SortObject, addToCurrentSort?: boolean): void
* Sorts the array with params passed in

---


######getCurrentOrderBy(): SortObject[]
* returns current orderBy used

---



######getCurrentFilter(): FilterObject[]
* Returns current filter used


---


######getElement(row: number): Entity
* Returns current element of row passed in


---


######group(grouping: GroupingObj[], keepExpanded?: boolean): void
* Groups the collection with params passed in


---


######groupCollapse(id: string): void
* Collapses all groups or just ID passes in


---

######groupExpand(id: string): void
* Expands all groups or just ID passed in

---


######getGrouping(): GroupingObj[]
* Returns grouping used

---


######addBlankRow(): void
* Adds blank row to top of diaplayed colelction and updates grid
* Todo: custom key will prb break this... need more testing

---


######unshift(data: any): void
* Added new enity to top of grid, no sorting or grouping after

---


######remove(rows?: any[]): any[]
* Removed rows from displayed collection and returns removed

---


######getCollectionStatus(): any
* Returns status(lengths) of collection/selection 
* collectionLength, filteredCollectionLength, selectionLength


---


######setLocaleCompare(code: string, options?: any): void {
* Sets local compare options to use with sorting
* http://stackoverflow.com/questions/3191664/list-of-all-locales-and-their-short-codes


---


######addEventListener(callback: Function): number
* Adds functions to callback array, this will be called when collection/selection event happens
* You will need to return true when function you pass in is called, else it will not be called again
* will come breaking changes to strings returned


---


######removeEventListener(id: number): void
* removes event listener

---