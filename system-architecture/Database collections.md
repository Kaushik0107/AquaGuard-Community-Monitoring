User collection 

{
  name,
  email,
  password,
  role: ["user", "moderator"],
  createdAt
}

Reports collection 

{
  userId,
  locationName,
  latitude,
  longitude,
  qualityLevel,
  contaminants,
  labReportFile,
  status,
  createdAt
}

Issues collection 

{
  userId,
  issueType,
  severity,
  description,
  photos,
  status,
  createdAt
}

Posts collection 

{
  title,
  content,
  category,
  authorId,
  likes,
  createdAt
}