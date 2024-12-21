# Code Card

### Import Component Shadcn
```javascript
import {
  Dialog,
  DialogContent,
  DialogTrigger,
} from "@/components/ui/dialog"

import { Button } from '@/components/ui/button';
```

### Dialog
```javascript
<Dialog>
	<DialogTrigger asChild>
	  <Button variant="outline">Open Dialog</Button>
	</DialogTrigger>
	<DialogContent className="p-0 border-none bg-transparent max-w-none w-auto">
	  <div className="relative h-[var(--card-height)] w-[var(--card-width)] bg-white p-[3px] rounded-md flex flex-col items-center justify-center">
	    <div className="card-content">
	      Contoh
	    </div>
	    <div
	      className="
		absolute
		bottom-0
		left-0
		right-0 
		w-3/4 h-3/4 mx-auto 
		scale-[0.8] 
		blur-[calc(var(--card-height)/6)]  
		bg-[linear-gradient(var(--rotate),#5ddcff,#3c67e3_43%,#4e00c2)] 
		[transition:opacity_0.5s] 
		[animation:spin_2.5s_linear_infinite] 
		[opacity:1]
		duration-500 z-[-1]"
	    />
	  </div>
	</DialogContent>
</Dialog>
```

## Tambahkan Code berikut ke `tailwind.config.js`
```javascript
keyframes: {
	spin: {
		'0%': { transform: 'rotate(0deg)' },
		'100%': { transform: 'rotate(360deg)' }
	}
},
```

## Note
- Ada penyesuain size ambient gradient dari `width dan height yang 100%` jadi `3/4` agar 
