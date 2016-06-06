class cool implements Runnable {
	public static void main(String[] args) {
		cool r = new cool();
		Thread a = new Thread(r);
		Thread b = new Thread(r);
		Thread c = new Thread(r);
		a.setName("thread a ");
		b.setName("thread b ");
		c.setName("thread c ");
		a.setPriority(Thread.MIN_PRIORITY);
		b.setPriority(Thread.NORM_PRIORITY);
		c.setPriority(Thread.MAX_PRIORITY);
		a.start();
		b.start();
		c.start();
	}
	
	public void run() {
		for (int i = 1; i <=5; i++)
 {
	System.out.println(Thread.currentThread().getName() + i + " is running");
	try {
	Thread.sleep(200);} 
  catch (InterruptedException e) {
  e.printStackTrace();
}
  }
    }	
}
