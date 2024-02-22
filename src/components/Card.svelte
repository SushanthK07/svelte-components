<!-- <div class="card"><slot /></div> -->

<!-- default content of slot -->
<!-- <div class="card"><slot>Default content</slot></div> -->

<div class="card">
  <div class="card-header">
    <slot name="header">Default header</slot>
  </div>
  <div class="card-content">
    <slot name="content">Default content</slot>
  </div>
  {#if $$slots.footer}
    <hr />
    <div class="card-footer">
      <slot name="footer" />
    </div>
  {/if}
</div>

<style>
  .card {
    padding: 20px;
    margin: 20px;
    background-color: #f4f4f4;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    max-width: 300px;
    text-align: center;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .card:hover {
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  }

  hr {
    width: 100%;
  }
</style>
