<script>
    let tasks = [];
  
    function addTask() {
      const newTask = prompt('Ingrese una nueva tarea');
      if (newTask) {
        tasks = [...tasks, newTask];
      }
    }
  
    function deleteTask(index) {
      tasks = tasks.filter((_, i) => i !== index);
    }
  </script>
  
  <div>
    <h2>Lista de tareas:</h2>
    <ul>
      {#each tasks as task, index}
        <li>{task} <button on:click={() => deleteTask(index)}>Eliminar</button></li>
      {/each}
    </ul>
    <button on:click={addTask}>Agregar Tarea</button>
  </div>
  