<template>
    <div class="input-message-block">
        <div class="input-message-container">
            <input type="text"
                v-model="message"
                @keyup.enter="sendMessage()"
                placeholder="Write your message here"
            >
            <button
                @click="sendMessage()"
                class="message_btn"
            >
                Send
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: "inputMessage",
    props: ["room"],
}
</script>

<style scoped>
.input-message-block {
    position: relative;
    height: 10px;
    margin: 1px;
}

.input-message-container {
    border-top: 1px solid #e6e6e6;
    display: grid;
    grid-column: 6;
}

.input-message-container > input {
    grid-column: span 5 / span 5;
    outline: none;
    padding: 1px;
}

.message_btn {
    place-self: end;
    --tw-bg-opacity: 1;
    background-color: rgba(107, 114, 128, var(--tw-bg-opacity));
    padding: 1px;
    margin-top: 1px;
    border-radius: 0.25rem;
    --tw-text-opacity: 1;
    color: rgba(255, 255, 255, var(--tw-text-opacity));
}

.message_btn:hover {
    --tw-bg-opacity: 1;
    background-color: rgba(29, 78, 216, var(--tw-bg-opacity));
}
</style>
