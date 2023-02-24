<template>
    <v-breadcrumbs :items="items">
        <template v-slot:title="{ item }">
            {{ item.title.toUpperCase() }}
        </template>
    </v-breadcrumbs>
</template>
<script>
export default {
    data: () => ({
        items: [
            {
                title: 'Dashboard',
                disabled: false,
                href: './',
            },
            {
                title: 'Link 1',
                disabled: false,
                href: './contato',
            },
            {
                title: 'Link 2',
                disabled: true,
                href: 'breadcrumbs_link_2',
            },
        ],
    }),
}
</script>
