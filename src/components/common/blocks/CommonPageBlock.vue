<template>
    <div class="page-block">
        <div
            v-if="$slots.title"
            class="page-block_title"
        >
            <slot name="title"/>
        </div>
        <slot/>
    </div>
</template>

<style scoped lang="scss">
.page-block {
    flex: 1 0 auto;

    width: 100%;
    padding: 24px;

    background: $darkgray950;
    border-radius: 16px;

    @include mobileOnly {
        padding: 8px;
    }

    &_title {
        margin-bottom: 16px;
        padding-bottom: 8px;

        font-size: 32px;
        font-weight: 600;
        color: $primary500;

        border-bottom: 1px solid varToRgba('lightgray150', 0.2);

        @include mobileOnly {
            font-size: 24px;
        }
    }
}
</style>
