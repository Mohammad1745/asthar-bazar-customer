<template>
  <tr :class="{subscribed: subPackage.subscribed}">
    <td class="td td-name">{{ subPackage.name }}</td>
    <td class="td">৳ {{ subPackage.charge }}</td>
    <td class="td">৳ {{ subPackage.capacity }}</td>
    <td class="td">{{ subPackage.subscribed ? 'Subcribed' : '---------' }}</td>
  </tr>
</template>

<script>
export default {
  name: "TableDataRow",
  props: ['subPackage'],
}
</script>

<style scoped lang="scss">
tr {
  display: flex;
  justify-content: space-between;
  padding: 0.25rem 2.5rem;

  &.subscribed {
    margin-top: 0.2rem;
    margin-bottom: 0.2rem;
    border: 2px solid #bbe432;
    background-color: rgba(0, 128, 0, 0.1);
    border-radius: 2rem;
  }
}
.td {
  flex-basis: 0;
  flex-grow: 1;
  display: flex;
  justify-content: center;
  align-items: center;

  &-name {
    justify-content: flex-start;
  }
}
</style>
