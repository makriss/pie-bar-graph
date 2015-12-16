#PIE BAR graph

Creates a bar graph, a pie chart and a legend

#Features
1. On hovering over a pie's sector, bar graph will display data only for that sector
2. On hovering out of pie chart, bar graph will display total of all sub categories
3. Legend displays the color code for each 'labelProp' and 'valueProp' and percent


#STEPS TO USE THE LIBRARY-
1. Create a container div and give it an id

2. Include d3 and bootstrap.min.css

3. Include pie-bar-graph.js and pie-bar-graph.css in your index file

4. Create a configuration object, dummy object is given below-
	```
    config = {
			width: 600, 				//width of the entire container
			height: 350, 				//height of the entire container
			valueProp: 'value',			//Object property under which numeric value is stored
			labelProp: 'name',			//Object property to be shown as label in legend
			subProp: 'categories',		//Property under which inner object is stored
			id: '#graph-chart',			//Id of the container element
			ratio: 0.4, 				//(Optional) Ratio of bar graph width to total 'width' (default: 0.5)
			marginV: 30					//(Optional) Vertical margin inside the containing element (default: 30)
		}
    ```

5. Instantiate the function and pass in config and data

#IMPORTANT POINTS-
1. Names should be same for label and value properties for both inner and outer object
2. Objects inside sub property array should be in same order throughout the passed in object
3. Object at level one will be shown in pie chart and inner object will be shown in bar graph. A dummy object is given in index.html
4. Outer Object (at level one) should necessarily have an 'id' property, which must be unique in the entire object hierarchy
5. Pass all the numeric values as number and not as string
