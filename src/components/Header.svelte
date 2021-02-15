<script>
  import { items } from "../stores";

  // console.log($items);
  $: itemCount = $items.length;
  $: completedItemCount = $items.filter(item => item.completed).length;
</script>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 20px;
    color: #ffffff;
    font-weight: bold;
    font-size: 1.5em;
    background: rgba(0, 0, 0, 0.1);
  }
</style>

<div class="header">
  <span>My To-Do List</span>
  <span>{ completedItemCount } / { itemCount }</span>
</div>