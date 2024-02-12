<script setup>
import GuestLayout from '@/Layouts/GuestLayout.vue'
import Label from '@/Components/InputLabel.vue' // 拡張子を .vue に修正
import Input from '@/Components/TextInput.vue' // 拡張子を .vue に修正

const emitTest = e =>console.log(e);
</script>

<template>
    <GuestLayout> <!-- コンポーネント名を修正 -->
        <Label value="件名"></Label>
        <Input modelValue="初期値が入ります"
        @update:modelValue="emitTest"></Input> <!-- 属性名を modelValue に修正 -->
    </GuestLayout>
</template>
