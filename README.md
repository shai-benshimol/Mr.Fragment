Mr.Fragment
===========

### Best Android Fragments Library
##### Manage your fragments effectively!


1. <a href="#implement-fragments-in-activity">Implement Fragments in Activity</a>
2. <a href="#implement-fragments-in-fragment">Implement Fragments in Fragment</a>
3. <a href="#download-library">Download Library</a>



===========


![Hii](https://github.com/shaibenshim/Mr.Fragment/blob/stuff/img.png?raw=true)
### Implement Fragments in Activity
===========
```Java
public class ExampleA extends FragmentActivity {
.....


          //Create a builder.
		FragmentBuilder builder = new FragmentBuilder();
		
		//Set your fragment, container and backStack.
		//Container = your inner view
		//Fragment = your custom  Fragment, ListFragment, MapFragment, DialogFragment...
		//backStack = true / false for your choice
		builder.set(R.id.fragment_a, new FragmentA(), true);
		builder.set(R.id.fragment_b, new FragmentB(), true);
		builder.set(R.id.fragment_c, new FragmentC(), false);
		
		//Create MrFragment
		MrFragment mrFragment = new MrFragment(this, builder);

		//Mr Fragment Methods:
		//1) Add.
		//2) Replace.
		//3) Remove.
		
		//Add
		mrFragment.add();

		// Replace Fragment A to Fragment C
		mrFragment.replace("FragmentA", new FragmentC(), true);

		// Remove Fragment B
		mrFragment.remove("FragmentB");


}
```
### Implement Fragments in Fragment
===========
```Java
public class ExampleB extends Fragment {
...
	public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
		
		//Infalte your view,
		View root = inflater.inflate(R.layout.in_fragment, null);
		
		//Reference to "Container" in your layout
		FrameLayout frame = (FrameLayout) root.findViewById(R.id.in_fragment);

		// The Point, call MrInFragment
		// Set context.
		// Set Container.
		// Set your Custom Fragment, ListFragment, MapFragment, Dialog Fragment...
		new MrInFragment(mContext, frame, new FragmentB());

		return root;
	}

}
```
### Download Library
[Mr. Fragment Library](https://github.com/shaibenshim/Mr.Fragment/blob/stuff/mr_fragment-1.0.jar?raw=true "Mr. Fragment")
