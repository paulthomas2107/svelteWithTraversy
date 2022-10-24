<script>

	
import FeedbackList from './components/FeedbackList.svelte';

  let feedback = [
	{
		id: 1,
		rating: 10,
		text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio hic nisi, facere ipsa optio debitis repellat iusto amet animi id laborum. Accusantium quaerat saepe veritatis, sunt iste ea magnam numquam.'
	},
	{
		id: 2,
		rating: 9,
		text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio hic nisi, facere ipsa optio debitis repellat iusto amet animi id laborum. Accusantium quaerat saepe veritatis, sunt iste ea magnam numquam.'
	},
	{
		id: 3,
		rating: 8,
		text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio hic nisi, facere ipsa optio debitis repellat iusto amet animi id laborum. Accusantium quaerat saepe veritatis, sunt iste ea magnam numquam.'
	}
  ]


  const deleteFeedback = (e) => {
	const itemId = e.detail
	feedback = feedback.filter((item) => item.id != itemId)
  }
</script>

<main class="container">
  <FeedbackList feedback={feedback} on:delete-feedback={deleteFeedback} />
	
</main>

<style>
  
  
</style>
