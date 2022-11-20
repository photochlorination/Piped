<script>
export default {
    props: {
        setting: String,
        label: String,
        model: String,
        change: Function,
    },
};
</script>

<template>
    <label class="pref" for="setting">
        <strong v-t="label" />
        <select v-bind:id="setting" v-bind:v-model="model" @change="change($event)">
            <option value="off">Disable</option>
            <option value="skip">Auto Skip</option>
            <option value="manual">Manual Skip</option>
            <option value="show">Show</option>
        </select>
    </label>
</template>
