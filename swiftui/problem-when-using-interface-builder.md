# Problem when using Interface Builder

### Interface Builder doesn't have close connection to the code

Let's create a page with a button that will print 'Hi' when we touch it:

<figure><img src="../.gitbook/assets/Screen Shot 2023-11-27 at 11.54.55.png" alt=""><figcaption></figcaption></figure>

We expected that the compiler could give us some warning but build was still successful after the `@IBAction` function had been commented:

<figure><img src="../.gitbook/assets/Screen Shot 2023-11-27 at 11.55.48.png" alt=""><figcaption></figcaption></figure>

It was because the IB file still keep the connection between the UIButton and the action:

<figure><img src="../.gitbook/assets/Screen Shot 2023-11-27 at 12.12.36.png" alt=""><figcaption></figcaption></figure>

Use the Object ID `VTR-lO-kyz` to look up the button in the IB file:&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-11-27 at 12.14.52.png" alt=""><figcaption><p>When we commented the action in the code, IB file didn't delete the action so the compiler didn't raise any warning.</p></figcaption></figure>

We just can know it from the crash at runtime.

### The code doesn't have close connection to the IB

Given that we have a custom cell called `FeedImageCell` in IB:&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-11-27 at 12.20.47.png" alt=""><figcaption></figcaption></figure>

In code, when we dequeue table view cells, we still have to typecast it like this:&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-11-27 at 12.22.27.png" alt=""><figcaption></figcaption></figure>
