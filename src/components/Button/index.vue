<template>
    <button>
        {{message}}
    </button>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Button extends Vue {
  @Prop() private msg!: string;

  get message(): string {
    return `Button message ${this.msg}`;
  }
}
</script>
