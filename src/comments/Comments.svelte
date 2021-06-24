<script>
    import { onMount } from "svelte";
    import BackButtonRow from "../common/BackButtonRow.svelte";
    import BookCover from "../common/BookCover.svelte";
    import Header from "../common/Header.svelte";
    import { httpGet, httpPut } from "../common/api.js";

    export let id;

    let book = {}
    onMount(async (_) => {
    const { data } = await httpGet("/" + id);
    book = data;
    });

    async function handleComments() {
    const toggledComments = {
      ...book,
      comments: !book.comments,
    };
    const { ok } = await httpPut("/comments" + book.id, toggledComments);
    if (ok) {
      book = toggledComments;
    }
  }
</script>

<BackButtonRow />

<Header element="h1" size="large">Comments</Header>

<BookCover {book} />


