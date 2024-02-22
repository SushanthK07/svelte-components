<!-- <div class="card"><slot /></div> -->

<!-- default content of slot -->
<div class="card"><slot>Default content</slot></div>

<style>
  .card {
    padding: 20px;
    margin: 20px;
    background-color: #f4f4f4;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    max-width: 300px;
  }

  .card:hover {
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  }
</style>
