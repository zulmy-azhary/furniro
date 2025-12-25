<script lang="ts">
	import Section from '@/components/layout/section.svelte';
	import MetaTitle from '@/components/misc/meta-title.svelte';
	import { Banner } from '@/components/ui/banner';
	import { Button } from '@/components/ui/button';
	import { Input } from '@/components/ui/input';
	import { Label } from '@/components/ui/label';
	import { Textarea } from '@/components/ui/textarea';

	const id = $props.id();
</script>

<MetaTitle title="Contact" />
<Banner title={{ name: 'Contact', path: '/contact' }} />

<Section class="flex flex-col items-center gap-y-16">
	<div class="text-center">
		<h4 class="text-4xl font-semibold text-slate-800">Get In Touch With Us</h4>
		<p class="mt-2 text-base text-slate-400 max-w-2xl font-light">
			For More Information About Our Product & Services. Please Feel Free To Drop Us An Email. Our
			Staff Always Be There To Help You Out. Do Not Hesitate!
		</p>
	</div>

	<div class="flex flex-col md:flex-row w-full justify-center gap-8 md:gap-4">
		<div class="flex basis-6/12 md:basis-5/12 lg:basis-4/12 flex-col gap-y-12">
			<div class="flex gap-x-3">
				<span class="icon-[ion--location-sharp] size-7"></span>
				<div class="space-y-1">
					<p class="text-2xl font-medium">Address</p>
					<div>
						<p>236 5th SE Avenue,</p>
						<p>New York NY10000, United States</p>
					</div>
				</div>
			</div>
			<div class="flex gap-x-3">
				<span class="icon-[ion--call] size-7"></span>
				<div class="space-y-1">
					<p class="text-2xl font-medium">Phone</p>
					<div>
						<p>Mobile: +(84) 546-6789</p>
						<p>Hotline: +(84) 456-6789</p>
					</div>
				</div>
			</div>
			<div class="flex gap-x-3">
				<span class="icon-[ion--time] size-7"></span>
				<div class="space-y-1">
					<p class="text-2xl font-medium">Working Time</p>
					<div>
						<p>Monday-Friday: 9:00 - 22:00</p>
						<p>Saturday-Sunday: 9:00 - 21:00</p>
					</div>
				</div>
			</div>
		</div>
		<form class="flex basis-6/12 flex-col gap-y-12">
			<div class="flex w-full max-w-xl flex-col gap-6">
				<Label for="name-{id}">Your Name</Label>
				<Input type="text" id="name-{id}" placeholder="John Doe" required />
			</div>
			<div class="flex w-full max-w-xl flex-col gap-6">
				<Label for="email-{id}">Email Address</Label>
				<Input type="email" id="email-{id}" placeholder="johndoe@example.com" required />
			</div>
			<div class="flex w-full max-w-xl flex-col gap-6">
				<Label for="subject-{id}">Subject</Label>
				<Input type="text" id="subject-{id}" placeholder="Your Subject" />
			</div>
			<div class="flex w-full max-w-xl flex-col gap-6">
				<Label for="message-{id}">Message</Label>
				<Textarea id="message-{id}" placeholder="Hi! i'd like to ask about..." required />
			</div>
			<Button type="submit" variant="accent" size="md" class="w-fit rounded-sm font-normal">
				Submit
			</Button>
		</form>
	</div>
</Section>
