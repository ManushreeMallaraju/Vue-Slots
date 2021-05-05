<template>
    <div class="frame">
        <!-- Named slot, along with Fallback Content -->
        <!-- <slot name="title">This is the default content, if nothing gets specified </slot>
        <h1>I'm a from helper</h1>
        <slot name="text"></slot> -->

        <!-- More on Named Slots, with <template></template> -->
        <header>
            <slot name="header"></slot>
        </header>
        <main>
            <slot></slot> <!-- Fallback/Default Slot -->
        </main>
        <footer>
            <slot name="footer"></slot>
        </footer>

        <!-- Scoped Slot-->
        <span>
            <slot v-bind:user="user">
                {{user.firstName}}
            </slot>
        </span>
    </div>
</template>

<script>

export default {
    data () {
    return {
     user:{
       firstName: "Manu",
       lastName: "Shree"
     }
    }
  }
}
</script>

<style scoped>

</style>