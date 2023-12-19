from pptx import Presentation
from pptx.util import Inches

# Create a presentation object
presentation = Presentation()

# Slide 1: Title Slide
slide_layout = presentation.slide_layouts[0]
slide_1 = presentation.slides.add_slide(slide_layout)
title = slide_1.shapes.title
subtitle = slide_1.placeholders[1]
title.text = "Debate on Financial Sustainability"
subtitle.text = "Gig Economy vs. Traditional Work"

# Slide 2: Introduction
slide_layout = presentation.slide_layouts[1]
slide_2 = presentation.slides.add_slide(slide_layout)
title = slide_2.shapes.title
content = slide_2.placeholders[1]
title.text = "Introduction"
content.text = "Today's discussion on the financial sustainability of the gig economy and freelancing."

# Slide 3: Key Points
slide_layout = presentation.slide_layouts[1]
slide_3 = presentation.slides.add_slide(slide_layout)
title = slide_3.shapes.title
content = slide_3.placeholders[1]
title.text = "Key Points"
content.text = "1. Flexibility vs. Uncertain Income\n2. Pros and Cons of Freelancing\n3. Opportunities and Challenges of Remote Work"

# Slide 4: Add Image
slide_layout = presentation.slide_layouts[5]  # Title and Content
slide_4 = presentation.slides.add_slide(slide_layout)
title = slide_4.shapes.title
content = slide_4.placeholders[1]
title.text = "The Gig Economy"
content.text = "Benefits of flexibility"
img_path = "path/to/your/image.jpg"  # Replace with the path to your image
content_pic = content.text_frame.add_picture(img_path, Inches(1), Inches(1), width=Inches(4))

# Slide 5: Add Video Placeholder
slide_layout = presentation.slide_layouts[5]  # Title and Content
slide_5 = presentation.slides.add_slide(slide_layout)
title = slide_5.shapes.title
content = slide_5.placeholders[1]
title.text = "Video: Remote Work Challenges"
content.text = "Discussing the isolation factor"
video_path = "path/to/your/video.mp4"  # Replace with the path to your video
content_video = content.text_frame.add_movie(video_path, Inches(1), Inches(1), width=Inches(4))

# Continue adding slides in a similar manner...

# Save the presentation
presentation.save("Debate_Presentation.pptx")
