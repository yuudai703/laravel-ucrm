<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

defineProps({
  items: Array
})

</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">商品一覧</h2>
        </template>
        <section class="text-gray-600 body-font" _msthidden="24">
  <div class="container px-5 py-24 mx-auto" _msthidden="24">
    <div class="flex pl-4 my-4 lg:w-2/3 w-full mx-auto" _msthidden="2">

      <button class="flex ml-auto text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded" _msttexthash="79859" _msthidden="1" _msthash="168">Button</button>
    </div>
    <div class="lg:w-2/3 w-full mx-auto overflow-auto" _msthidden="20">
      <table class="table-auto w-full text-left whitespace-no-wrap" _msthidden="20">
        <thead _msthidden="4">
          <tr _msthidden="4">
            <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100 rounded-tl rounded-bl" _msttexthash="44161" _msthidden="1" _msthash="147">id</th>
            <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100" _msttexthash="58448" _msthidden="1" _msthash="148">商品名</th>
            <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100" _msttexthash="94432" _msthidden="1" _msthash="149">価格</th>
            <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100" _msttexthash="58734" _msthidden="1" _msthash="150">ステータス</th>
            <th class="w-10 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100 rounded-tr rounded-br"></th>
          </tr>
        </thead>
        <tbody _msthidden="16">
          <tr _msthidden="4" v-for=" item in items" :key="item.id">
            <td class="px-4 py-3 border-b-2 border-groy-200" _msttexthash="62374" _msthidden="1" _msthash="151">{{ item.id }}</td>
            <td class="px-4 py-3 border-b-2 border-groy-200" _msttexthash="46852" _msthidden="1" _msthash="152">{{ item.name }}</td>
            <td class="px-4 py-3 border-b-2 border-groy-200" _msttexthash="26858" _msthidden="1" _msthash="153">{{ item.price }}</td>
            <td class="px-4 py-3 border-b-2 border-groy-200" _msttexthash="43173" _msthidden="1" _msthash="154">
              <span v-if="item.is_selling === 1">販売中</span>
              <span v-if="item.is_selling === 0">停止中</span>
            </td>
          </tr>
        </tbody>
      </table>
    </div>

  </div>
</section>
    </AuthenticatedLayout>
</template>
