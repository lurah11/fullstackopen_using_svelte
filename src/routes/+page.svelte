<script>
   import Header from '$lib/Header.svelte';
   import Content from '$lib/Content.svelte'; 
   import Total from '$lib/Total.svelte';
   const course = {
    name: 'Half Stack application development',
    parts: [
      {
        name: 'Fundamentals of React',
        exercises: 10
      },
      {
        name: 'Using props to pass data',
        exercises: 7
      },
      {
        name: 'State of a component',
        exercises: 14
      }
    ]
  }

</script>


<h1>EXERCISE 1.3 TO 1.5</h1>

<Header name={course.name} />
<Content parts = {course.parts}/>
<Total parts = {course.parts}/>

