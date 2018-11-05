<template>
      <tr>
        <td>{{user.id}}</td>
        <td>{{user.name}}</td>
        <td>{{user.gender}}</td>
        <td>{{user.email}}</td>
        <td>{{user.online}}</td>
      </tr>
</template>

<script>

export default {
    props: {
        user:{
            type: Object,
            required: true
        }
    }
}
</script>
