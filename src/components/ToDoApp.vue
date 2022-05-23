<template>
  <div class="container">
    <h2 class="text-center mt-5">My Vue ToDo App</h2>

    <div class="d-flex">
      <input type="text" placeholder="Enter task" class="form-control" />
      <button class="btn btn-success rounded-0">Submit</button>
    </div>

    <table class="table table-bordered mt-5">
      <thead>
        <tr>
          <th scope="col">Task</th>
          <th scope="col">Status</th>
          <th scope="col">#</th>
          <th scope="col">#</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(task, index) in tasks" :key="index">
          <td>Steal bananas from the store</td>
          <td>To-Do</td>
          <td>
            <div class="text-center">
              <span class="fa fa-pen"></span>
            </div>
          </td>
          <td>
            <div class="text-center">
              <span class="fa fa-trash"></span>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data() {
    return {
      tasks: [
        {
          name: "banana steal",
          status: "to-do",
        },
        {
          name: "choco eat",
          status: "in-progres",
        },
      ],
    };
  },
};
</script>

<style scoped></style>
